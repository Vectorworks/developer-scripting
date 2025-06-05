# vsoStateGetPos

## Description
Used to determine if an object has been moved. Returns True if the object was moved and the distance the object was moved in mm. See [[VS:Parametric State Notifications#vsoStateGetPos]]

This function should be called during the parametric reset event: <code>3: {kParametricRecalculate}</code>

```pascal
FUNCTION vsoStateGetPos(
				hObj        : HANDLE;
				VAR outX    : REAL;
				VAR outY    : REAL;
				VAR outZ    : REAL;
				VAR outIs3D : BOOLEAN): BOOLEAN;
```

```python
def vs.vsoStateGetPos(hObj):
    return (BOOLEAN, outX, outY, outZ, outIs3D)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|Handle to the parametric object. Obtained by call to [GetCustomObjectInfo](GetCustomObjectInfo.md)|
|outX|REAL|Output parameter. Moved distance in mm.|
|outY|REAL|Output parameter. Moved distance in mm.|
|outZ|REAL|Output parameter. Moved distance in mm.|
|outIs3D|BOOLEAN|Output parameter. Is 3D operation.|

## Remarks
Returns the distance moved (NOT the previous x,y,z location) in mm.

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
 
      IF vsoStateGetPos( objectHand, x, y, z, is3D ) THEN BEGIN
        MoveTo( 0,-10mm );
        CreateText( Concat( 'Object just moved! offset=(', x, ' ,', y, ' ,', y, ' z', z, ') is3DMove=', is3D ) );
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
Availability: from Vectorworks2009
This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
