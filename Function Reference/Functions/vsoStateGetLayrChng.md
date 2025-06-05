# vsoStateGetLayrChng

## Description
Used to determine if the layer scale have changed. See [[VS:Parametric State Notifications#vsoStateGetLayrChng]]

This function should be called during the parametric reset event: <code>3: {kParametricRecalculate}</code>

```pascal
FUNCTION vsoStateGetLayrChng(
				hObj             : HANDLE;
				VAR outOldScale  : REAL;
				VAR outNewScale  : REAL;
				VAR outScaleText : BOOLEAN): BOOLEAN;
```

```python
def vs.vsoStateGetLayrChng(hObj):
    return (BOOLEAN, outOldScale, outNewScale, outScaleText)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|Handle to the parametric object. Obtained by call to [GetCustomObjectInfo](GetCustomObjectInfo.md)|
|outOldScale|REAL|Output parameter. Old layer scale.|
|outNewScale|REAL|Output parameter. New layer scale.|
|outScaleText|BOOLEAN|Output parameter. Does the new scale affect texts.|

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
      result := SetObjPropVS( 2, TRUE ); {kObjXPropHasLayerScaleDeps}
    END;	

    44: {kObjOnAddState}
    BEGIN
      message := vsoStateAddCurrent( objectHand, message );
    END;

    3: {kParametricRecalculate}
    BEGIN
      MoveTo( 5mm, 8mm );
      CreateText( 'State events received after the last kParametricRecalculate:' );

      IF vsoStateGetLayrChng( objectHand, oldScale, newScale, scaleText ) THEN BEGIN
        MoveTo( 0,-60mm );
        CreateText( Concat( 'Layer changed! oldScale=', oldScale, ' newScale=', newScale, ' scaleText=', scaleText ) );
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
