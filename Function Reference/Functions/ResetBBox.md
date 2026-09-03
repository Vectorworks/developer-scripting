# ResetBBox

## Description
Procedure ResetBBox forces the bounding box information for the specified object to be recomputed based on the objects' current geometry. 

Call this procedure after modifying an object to force a redraw of the object.

```pascal
PROCEDURE ResetBBox(h : HANDLE);
```

```python
def vs.ResetBBox(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Forces the bouding box information for object h to be recomputed based on current geometry.

This doesn't seem to work on symdefs.

## Examples
```pascal
BEGIN
ResetBBox(MarkerH);
GetBBox(MarkerH,p1X, p1Y, p2X, p2Y);
IF ABS(p2y) > Abs(p1y) THEN
	p1y := Abs(p2y)
ELSE

		IF (hSub <> NIL) THEN HSub2 := finsymdef(hSub);
		foreachobjectinlist(Scaleprim, 0, 2, HSub2);
		SetName(hSub, concat(getSDName(hSub), kDash, num2str(0, factor)));
	END;
	resetbbox(GetObject(concat(SDName, kDash, num2str(0, Scalefactor))));
	SetOrigin(xO, yO);
END;

BEGIN
planarRef := GetPlanarRef( MarkerH );
SetPlanarRef( MarkerH, 0 );
ResetBBox(MarkerH);
GetBBox(MarkerH,p1X, p1Y, p2X, p2Y);
SetPlanarRef( MarkerH, planarRef );
IF (p1Y >= 0) AND (p2Y >= 0) THEN
	p1Y := Abs(p2Y - p1Y )
```
```python
import vs

# Procedure ResetBBox forces the bounding box information for the specified
# object to be recomputed based on the objects' current geometry.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.ResetBBox(h)
```

## Version
Availability: from All Versions

## Category
* [Object Editing](../Categories/Object%20Editing.md)
