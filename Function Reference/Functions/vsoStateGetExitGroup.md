# vsoStateGetExitGroup

## Description
Used to determine if exit from group have happened. See [[VS:Parametric State Notifications#vsoStateGetExitGroup]]

This function should be called during the parametric reset event: <code>3: {kParametricRecalculate}</code>

Group types:
* kObjXPropEditGroupDefault = 0
* kObjXPropEditGroupProfile = 1
* kObjXPropEditGroupPath = 2
* kObjXPropEditGroupCustom = 3

```pascal
FUNCTION vsoStateGetExitGroup(
				hObj           : HANDLE;
				VAR outGrpType : LONGINT): BOOLEAN;
```

```python
def vs.vsoStateGetExitGroup(hObj):
    return (BOOLEAN, outGrpType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|Handle to the parametric object. Obtained by call to [GetCustomObjectInfo](GetCustomObjectInfo.md)|
|outGrpType|LONGINT|Output parameter. Return the group type.|

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

      IF vsoStateGetExitGroup( objectHand, grpType ) THEN BEGIN
        MoveTo( 0,-40mm );
        IF grpType = 0 THEN       CreateText( 'Object exited from edit group! Exited from: Default Group!' )
        ELSE IF grpType = 1 THEN  CreateText( 'Object exited from edit group! Exited from: Profile Group!' )
        ELSE IF grpType = 2 THEN  CreateText( 'Object exited from edit group! Exited from: Path Group!' )
        ELSE IF grpType = 3 THEN  CreateText( 'Object exited from edit group! Exited from: Custom Group!' )
        ELSE                      CreateText( 'Object exited from edit group! Exited from: Uknown Group!' );
      END;
    END;
```
#### Python ####
```python

```

```pascal
		END;
END;
	{ check if event is exit from edit group. }
IF vsoStateGetExitGroup( objHand, grpType ) THEN BEGIN
	IF ( grpType = 1 ) THEN BEGIN
		{ Old objects need to be reset on exiting the profile group }
		IF Str2Num(GetRField(objHand,objName,'__version')) < 1750 THEN BEGIN
			bExitEditGroup := TRUE;
			{ First clear everything inside the parametric object (except the profie group) }
			DeleteObjects;
			{ Reset the object,without handrails if necessary in order to save the edited profile group }
			Reset(TRUE);
```
```python
result = vs.vsoStateGetExitGroup(h)
```

## See Also
[Parametric State Notifications](../../Common/Tasks/Parametrics/Parametric%20State%20Notifications.md) | [vsoStateAddCurrent](vsoStateAddCurrent.md)

[vsoStateGetPos](vsoStateGetPos.md) | [vsoStateGetRot](vsoStateGetRot.md) | [vsoStateGetParamChng](vsoStateGetParamChng.md) | [vsoStateGetObjChng](vsoStateGetObjChng.md) | [vsoStateGetLayrChng](vsoStateGetLayrChng.md) | [vsoStateGetExitGroup](vsoStateGetExitGroup.md) | [vsoStateGetNameChng](vsoStateGetNameChng.md)

## Version
Availability: from Vectorworks 2009

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
