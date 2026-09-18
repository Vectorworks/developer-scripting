# SetPlanarRefIDToGround

## Description
Set the specified object on the ground plane. This function is to be used inside parametric objects to place objects on the local coordinate system's ground of the parametric.

```pascal
PROCEDURE SetPlanarRefIDToGround(h : HANDLE);
```

```python
def vs.SetPlanarRefIDToGround(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the object.|

## Examples
```pascal
BEGIN
	z := z + deltaZ;
	SetPlanarRefIDToGround(curveHand [cnt]);
	nurbsHand [cnt] := ConvertToNURBS(curveHand [cnt], FALSE);
	Move3DObj(nurbsHand [cnt], 0, 0, z);
END;

BEGIN
	poly_h := CreateDuplicateObject( temp2_hp, GetLayer( temp2_hp ) );
	SetPlanarRefIDToGround(poly_h);
END

IF (getcurrentplanarrefID = 0) THEN SetPlanarRefIDToGround(poly2D_h);
GetLayerElevation(getlayer(poly2D_h),elev,thk);
Move3DObj(poly2D_h,0,0,elev/25.4);
```
```python
import vs

# Set the specified object on the ground plane.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.SetPlanarRefIDToGround(h)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Object Info](../Categories/Object%20Info.md)
