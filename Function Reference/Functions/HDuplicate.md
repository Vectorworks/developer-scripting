# HDuplicate

## Description
Duplicates and moves an object by the offsets specified.

```pascal
FUNCTION HDuplicate(
				objectHandle : HANDLE;
				x            : REAL;
				y            : REAL): HANDLE;
```

```python
def vs.HDuplicate(objectHandle, x, y):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the object to duplicate|
|x|REAL|X-coordinate of distance object should be shifted from original location|
|y|REAL|Y-coordinate of distance object should be shifted from original location|

## Examples
```pascal
if ( GetType(h) = 68 ) then BEGIN
	h1 := WallFootPrint(h);
	ok := TRUE;
END else if (GetType(h) = 71) & (GetObjectVariableInt(h, 172) = 3) then BEGIN
	h1 := HDuplicate(FIn3D(h), 0, 0);
	ok := TRUE;
END;

BEGIN
	rectH := polyH;
	SetDSelect (rectH);
	polyH := ConvertToPolyline( HDuplicate( polyH, 0, 0 ) );
END;

BEGIN
	tempH := ConvertToPolyline(HDuplicate(objH, 0, 0));
	getProperties_Polyline (tempH, area, perim, xC, yC, Ixx, Iyy, Cxx, Cyy);
	DelObject (tempH);
	area := HArea(objH);
	perim := HPerim(objH);
```
```python
import vs

# Duplicates and moves an object by the offsets specified.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
x = 0.0
y = 0.0

objHandle = vs.HDuplicate(objectHandle, x, y)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Object Editing](../Categories/Object%20Editing.md)
