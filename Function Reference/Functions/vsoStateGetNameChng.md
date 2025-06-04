# vsoStateGetNameChng

## Description
Used to determine if the object name have changed. See [[VS:Parametric State Notifications#vsoStateGetNameChng]]

This function should be called during the parametric reset event: <code>3: {kParametricRecalculate}</code>

```pascal
FUNCTION vsoStateGetNameChng(
				hObj           : HANDLE;
				VAR outOldName : STRING;
				VAR outNewName : STRING): BOOLEAN;
```

```python
def vs.vsoStateGetNameChng(hObj):
    return (BOOLEAN, outOldName, outNewName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|Handle to the parametric object. Obtained by call to [[VS:GetCustomObjectInfo]]|
|outOldName|STRING|Output parameter. Old object name.|
|outNewName|STRING|Output parameter. New object name.|

## Remarks
[[User:CBM-c-|_c_]] (2016.05.14): Warning, actions that modify an object's name don't trigger a regen event, so vsoStateGetNameChng won't detect name changes until next regen. Actions that change the name can be:
* editing the name object in the Data tab of the Object Info Palette
* modifying the object's name from within the script in any fashion
* automatic name deletion in case of name collision.
Setting your event enabled object to regen On Move is the best approach, as far as I see (even a copy in place is a move, for VW).

## Examples
==== VectorScript ====
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

      IF vsoStateGetNameChng( objecthand, oldName, newName ) THEN BEGIN
        MoveTo( 0, -70mm );
        CreateText( Concat( 'Obj name changed! oldName=', oldName, ' newName=', newName  ) );
      END;

    END;

    41: {kObjOnWidgetPrep}
    BEGIN
      vsoSetEventResult(-8); { kObjectEventHandled }
    END;
```
==== Python ====
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
