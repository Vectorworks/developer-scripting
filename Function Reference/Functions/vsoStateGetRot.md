# vsoStateGetRot

## Description
Used to determine of the object has been rotated. See [[VS:Parametric State Notifications#vsoStateGetRot]]

This function should be called during the parametric reset event: <code>3: {kParametricRecalculate}</code>

```pascal
FUNCTION vsoStateGetRot(
				hObj           : HANDLE;
				VAR outDiffAng : REAL;
				VAR outIs3D    : BOOLEAN): BOOLEAN;
```

```python
def vs.vsoStateGetRot(hObj):
    return (BOOLEAN, outDiffAng, outIs3D)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|Handle to the parametric object. Obtained by call to [[VS:GetCustomObjectInfo]]|
|outDiffAng|REAL|Output parameter. Difference between the new and the old angles. Negative if old angle was bigger value.|
|outIs3D|BOOLEAN|Output parameter. Was a 3D operation.|

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

      IF vsoStateGetRot( objectHand, diffAng, is3D ) THEN BEGIN
        MoveTo( 0,-20mm );
        CreateText( Concat( 'Object just rotated! diff=', diffAng,' deg is3DMove=', is3D ) );
      END;
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
