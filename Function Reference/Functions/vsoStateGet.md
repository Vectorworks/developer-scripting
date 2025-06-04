# vsoStateGet

## Description
Checks if the passed parametric object have received specific 'state' event before this reset event. [[VS:Parametric State Notifications#vsoStateGet]]

This function should be called during the parametric reset event: <code>3: {kParametricRecalculate}</code>

```pascal
FUNCTION vsoStateGet(
				hObj  : HANDLE;
				state : INTEGER): BOOLEAN;
```

```python
def vs.vsoStateGet(hObj, state):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|Handle to the parametric object. Obtained by call to [[VS:GetCustomObjectInfo]]|
|state|INTEGER|State Identifier which you want to check.|

## Remarks
State constants are:
:[[VS:Parametric State Notifications#kCreatedReset|kCreatedReset]] = 0;
:[[VS:Parametric State Notifications#kMovedReset|kMovedReset]] = 1;
:[[VS:Parametric State Notifications#kRotatedReset|kRotatedReset]] = 2;
:[[VS:Parametric State Notifications#kParameterChangedReset|kParameterChangedReset]] = 3;
:[[VS:Parametric State Notifications#kObjectChangedReset|kObjectChangedReset]] = 4;
:[[VS:Parametric State Notifications#kLayerChangedReset|kLayerChangedReset]] = 5;
:[[VS:Parametric State Notifications#kExitFromEditGroup|kExitFromEditGroup]] = 6;
:[[VS:Parametric State Notifications#kObjectNameChanged|kObjectNameChanged]] = 7;

## Examples
#### VectorScript ####
```pascal
BEGIN
  result := GetCustomObjectInfo(objectName, objectHand, recordHand, wallHand);
  vsoGetEventInfo(theEvent, message );

  CASE theEvent OF
    5: {kObjOnInitXProperties}
    BEGIN
      {enable eventing for this plug-in}
      SetPrefInt( 590, 1 ); {varParametricEnableStateEventing, kParametricStateEvent_ResetStatesEvent}
      result := SetObjPropVS(18, TRUE); {kObjXPropAcceptStates}
    END;	

    44: {kObjOnAddState}
    BEGIN
      message := vsoStateAddCurrent( objectHand, message );
    END;

    3: {kParametricRecalculate}
    BEGIN
      MoveTo( 5mm, 8mm );
      CreateText( 'State events received after the last kParametricRecalculate:' );

      IF vsoStateGet( objectHand, 0 {ObjectState::kCreatedReset} ) THEN BEGIN
        MoveTo( 0, 0 );
        CreateText( 'Object just created!' );
      END;
    END;
```
#### Python ####
```python

```

## See Also
[Parametric State Notifications](Parametric%20State Notifications.md) | [vsoStateAddCurrent](vsoStateAddCurrent.md)

[vsoStateGetPos](vsoStateGetPos.md) | [vsoStateGetRot](vsoStateGetRot.md) | [vsoStateGetParamChng](vsoStateGetParamChng.md) | [vsoStateGetObjChng](vsoStateGetObjChng.md) | [vsoStateGetLayrChng](vsoStateGetLayrChng.md) | [vsoStateGetExitGroup](vsoStateGetExitGroup.md) | [vsoStateGetNameChng](vsoStateGetNameChng.md)

## Version
Availability: from Vectorworks 2009
This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
