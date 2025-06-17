By [Vladislav Stanev](mailto:vstanev@nemetschek.net)

## What's that

State Notification mechanism allows the plug-in to receive notifications for changes that happen to the parametric object.

For example, `kParametricRecalculate(5)` event is sent to the plug-in to update the parametric object, but there is no information on what exactly happened that needs an update.

Currently, the following states are supported:

### Pre-reset states

Giving information on what happened before the reset:

- **`kCreatedReset` (0)** -- The parametric has just been created.
- **`kMovedReset` (1)** -- The parametric has been moved (only if reset on move flag is on).
- **`kRotatedReset` (2)** -- The parametric has been rotated (only if reset on rotate flag is on).
- **`kParameterChangedReset` (3)** -- Parameter has been changed.
- **`kObjectChangedReset` (4)** -- Attributes change reset.
- **`kLayerChangedReset` (5)** -- Layer scale or position has been changed.

### States that don't cause automatic reset

- **`kExitFromEditGroup` (6)** -- The parametric profile or other special group has been changed.
- **`kObjectNameChanged` (7)** -- Parametric object name changed – sent when the object name changes.

**Note:** The states event is informative. This means that when receiving non-reset states, a plug-in should not cause a reset or call other VectorWorks functions.

## Setting up

In order to create a custom user interface for the parametric object, your parametric plug-in should be event-enabled.

Then you need to handle the `kObjOnInitXProperties(5)`.

```vs
case kObjOnInitXProperties: {
BEGIN {MAIN}
  result := GetCustomObjectInfo(objectName, objectHand, recordHand, wallHand);
  vsoGetEventInfo(theEvent, message );

  CASE theEvent OF
    5: {kObjOnInitXProperties}
    BEGIN
      { 1. Enable application to send out those flags
           to the plug-ins who need them }
      SetPrefInt( 590, 1 ); {varParametricEnableStateEventing, kParametricStateEvent_ResetStatesEvent}

      { 2. Enable the plug-in to receive states events (regular states) }
      result := SetObjPropVS(18, TRUE); {kObjXPropAcceptStates}
    END;
```

### 1. Enable events in the application

Using program flags, you should enable the application to send out those events to the plug-ins.

This is intended to optimize performance if there are no plug-ins that are interested in those events.

### 2. Enable extended standard states property

Property `kObjXPropAcceptStates(18)` must be set to **TRUE** to enable receiving standard states for this parametric.

## Receiving States: `kParametricAddState (44)`

During this event, the user MUST only call `vsoStateAddCurrent` nothing else!

```vs
  vsoGetEventInfo( theEvent, message );

  ...

  44: {kObjOnAddState}
  BEGIN
    message := vsoStateAddCurrent( objectHand, message );
  END;
```

## Reset event

When `kParametricRecalculate(3)` event is received, the VectorScript plug-in can recognize if a state has occurred by calling the appropriate function according to the event:

In order to receive correct information on received states in between resets, **IT IS EXTREMELY IMPORTANT** to call `vsoStateClear` at the end of the reset event:

```vs
  3: {kParametricRecalculate}
  BEGIN
    { ... }

    vsoStateClear( objectHand );
  END;
```

### `kCreatedReset`

This state doesn't have data attached, so you can use the general function `vsoStateGet` to check if this state has been sent.

```pas
IF vsoStateGet( objectHand, 0 {kCreatedReset} ) THEN BEGIN
```

### `kMovedReset`

Returns TRUE if the event has been received `vsoStateGetPos` and obtains information on the event.

```vs
FUNCTION vsoStateGetPos(hObj: HANDLE; VAR outX: REAL; VAR outY: REAL; VAR outZ: REAL; VAR outIs3D: BOOLEAN) : BOOLEAN;
```

```vs
IF vsoStateGetPos( objectHand, x, y, z, is3D ) THEN BEGIN
```

### `kRotatedReset`

Returns TRUE if the event has been received `vsoStateGetRot` and obtains information on the event.

```vs
FUNCTION vsoStateGetRot(hObj: HANDLE; VAR outDiffAng: REAL; VAR outIs3D: BOOLEAN) : BOOLEAN;
```

```vs
IF vsoStateGetRot( objectHand, diffAng, is3D ) THEN BEGIN
```

### `kParameterChangedReset`

Returns TRUE if the event has been received `vsoStateGetParamChng` and obtains information on the event.

```vs
FUNCTION vsoStateGetParamChng(hObj: HANDLE; VAR outWidgID: LONGINT; VAR outPrmIdx: INTEGER; VAR outOldVal: STRING) : BOOLEAN;
```

```vs
IF vsoStateGetParamChng( objectHand, widgID, prmIndex, oldValue ) THEN BEGIN
```

### `kObjectChangedReset`

Returns TRUE if the event has been received `vsoStateGetObjChng` and obtains information on the event.

```vs
FUNCTION vsoStateGetObjChng(hObj: HANDLE; VAR outChangeID: LONGINT) : BOOLEAN;
```

```vs
IF vsoStateGetObjChng( objectHand, changeID ) THEN BEGIN
```

### `kLayerChangedReset`

Returns TRUE if the event has been received `vsoStateGetLayrChng` and obtains information on the event.

```vs
FUNCTION vsoStateGetLayrChng(hObj: HANDLE; VAR outOldScale: REAL; VAR outNewScale: REAL; VAR outScaleText: BOOLEAN) : BOOLEAN;
```

```vs
IF vsoStateGetLayrChng( objectHand, oldScale, newScale, scaleText ) THEN BEGIN
```

### `kExitFromEditGroup`

Returns TRUE if the event has been received `vsoStateGetExitGroup` and obtains information on the event.

```vs
FUNCTION vsoStateGetExitGroup(hObj: HANDLE; VAR outGrpType: LONGINT) : BOOLEAN;
```

```vs
IF vsoStateGetExitGroup( object Hand, grpType ) THEN BEGIN
```

Provides the group type of the group that the user just exited. The types are one of the following:
- `kObjXPropEditGroupDefault = 0`
- `kObjXPropEditGroupProfile = 1`
- `kObjXPropEditGroupPath = 2`
- `kObjXPropEditGroupCustom = 3`

**Note:** "Exit Group" doesn't send a reset event. This means that you have to explicitly reset the object upon receiving the state event:

```pas
44: {kObjOnAddState}
BEGIN
  res := vsoStateAddCurrent( object Hand, message );
  IF vsoStateGetExitGroup( object Hand, grpType ) THEN BEGIN
    {readd it so the reset could be able to get it}
    res := vsoStateAddCurrent( object Hand, message );
    ResetObject( object Hand );
  END;
END;
```

### `kObjectNameChanged`

Returns TRUE if the event has been received `vsoStateGetNameChng` and obtains information on the event.

```vs
FUNCTION vsoStateGetNameChng(hObj: HANDLE; VAR outOldName: STRING; VAR outNewName: STRING) : BOOLEAN;
```

```vs
IF vsoStateGetNameChng( object Hand, oldName, newName ) THEN BEGIN
```

## Example

Full example: [VSEventingObject.zip](examples/VSEventingObject.zip)
