# GetObjectVariableBoolean

## Description
Returns the ON-OFF status of a VectorWorks object property. 

For specific object selector index values, see the [Script Appendix](../Appendix/pages/Appendix%20G%20-%20Object%20Selectors.md).

```pascal
FUNCTION GetObjectVariableBoolean(
				h     : HANDLE;
				index : INTEGER): BOOLEAN;
```

```python
def vs.GetObjectVariableBoolean(h, index):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|index|INTEGER|Object property index.|

## Remarks
From Julian: Appears to be unreliable for walls because it returns a different result depending on the view. Walls always report false for 2D, but only report true for 3D if in a 3D view.

## Examples
#### VectorScript ####
```pascal
castShadow:= GetObjectVariableBoolean(h,53);
```
#### Python ####
```python
castShadow = vs.GetObjectVariableBoolean(h,53)
```

```pascal
BEGIN
	recordH := GetRecord (NIL, i);
	IF NOT IsPluginFormat (recordH) AND NOT GetObjectVariableBoolean(recordH, 700) THEN  {700 is whether or not the object is locked}
	BEGIN
		j := j + 1;
		ALLOCATE gRecordN [1..j];
		gRecordN [j] := GetName (recordH);
	END;

hideStyleParms := GetObjectVariableBoolean( parmHand, 1168 );
doorHandStyleType := GetParamStyleType( parmHand, '__DoorHandle' );
drawerHandStyleType := GetParamStyleType( parmHand, '__DrawerHandle' );

{ if round wall, check if clockwise }
IF (IsArcBasedWall(gWallHand)) & (NOT GetObjectVariableBoolean(gWallHand, 570)) THEN
BEGIN
	GetSegPt2(gWallHand, begwall_pt.x, begwall_pt.y);
	GetSegPt1(gWallHand, endwall_pt.x, endwall_pt.y);
END;
```
```python
import vs

# Returns the ON-OFF status of a VectorWorks object property.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1

ok = vs.GetObjectVariableBoolean(h, index)
if ok:
    vs.Message('GetObjectVariableBoolean succeeded')
else:
    vs.Message('GetObjectVariableBoolean failed')
```

## Version
Availability: from VectorWorks9.0

## Category
* [Object Info](../Categories/Object%20Info.md)
