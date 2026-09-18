# ClosestPoints

## Description
Returns the points on two objects where the shortest distance between those objects occurs. Should support all VW primitives, including polylines and NURBS. Would be nice if it supported groups, symbols, and PIOs. Would also be nice if it supported 3D.

```pascal
PROCEDURE ClosestPoints(
				h1           : HANDLE;
				h2           : HANDLE;
				VAR pt1      : VECTOR;
				VAR pt2      : VECTOR;
				VAR touching : BOOLEAN);
```

```python
def vs.ClosestPoints(h1, h2):
    return (pt1, pt2, touching)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h1|HANDLE|   |
|h2|HANDLE|   |
|pt1|VECTOR|   |
|pt2|VECTOR|   |
|touching|BOOLEAN|   |

## Examples
```pascal
for cnt1 := 1 to spaceCnt do BEGIN
	for cnt2 := (cnt1 + 1) to spaceCnt do BEGIN
		Message(GetPlugInString(5015), cnt1, ' & ', cnt2, '.'); {Figuring interior walls between spaces }
		if Intersect2Rects(spaces[cnt1].ul, spaces[cnt1].lr, spaces[cnt2].ul, spaces[cnt2].lr) then BEGIN
			ClosestPoints(spaces[cnt1].h, spaces[cnt2].h, pt1, pt2, boo);
			if boo then BEGIN
				{Use IntersectSurface to find the overlapping portion.}
				medAxis := NIL;
				h1 := NextObj(spaces[cnt2].h);
```
```python
import vs

# Returns the points on two objects where the shortest distance between those
# objects occurs.
h1 = vs.FSActLayer()  # handle to the first selected object on the active layer
h2 = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

pt1, pt2, touching = vs.ClosestPoints(h1, h2)
vs.Message('ClosestPoints returned: ' + str((pt1, pt2, touching)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
