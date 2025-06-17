# GetPolyPt

## Description
Procedure GetPolyPt returns the coordinates of a specified vertex of the referenced object.

```pascal
PROCEDURE GetPolyPt(
				objectHd  : HANDLE;
				index     : INTEGER;
				VAR pX,pY : REAL);
```

```python
def vs.GetPolyPt(objectHd, index):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to polygon.|
|index|INTEGER|Index of vertex (range of 1 to n).|
|p|REAL|Returns coordinates of vertex.|

## Remarks
(*_c_*, 2022.01.18) In VS Python this routine returns a 2-dimensional tuple. Warning: Most Math - Vector routines require a 3-dimensional tuple, failing to init a third item in VW before 2023 (vs.Vec2Ang, for example, returns gibberish on 2-d tuples). You will need to make sure that a third item exists.
<code lang="py">
# test GetPolyPt
p = (0, 0, 0)
vs.AlrtDialog( 'init tuple: ' + str(len(p)) ) # 3 items
p = vs.GetPolyPt(vs.FSActLayer(), 1) # take care to have a polygon selected
vs.AlrtDialog( 'after GetPolyPt: ' + str(len(p)) ) # 2 items?!?
```

(*_c_*, 2010.12.22) Since the introduction of rotated rectangles, it doesn't turn them into polygons any longer. The routine fails with warning, as expected. 

(Charles Chandler, 2001 Jan. 25): Doesn't work on rectangles, unless you rotate them, which turns them into polygons.

## Examples
#### VectorScript ####
```pascal
FOR i := 1 to GetVertNum(thePoly) DO
    GetPolyPt(thePoly, i, vertX, vertY);
```
#### Python ####
```python
def Example():
    obj = vs.FSActLayer()
    for vertexNum in range(1, vs.GetVertNum(obj)):
        ptVt = vs.GetPolyPt(obj, vertexNum)
        vs.TextOrigin(ptVt[0], ptVt[1])
        vs.CreateText(vs.Concat('vNum: ', vertexNum))
Example()
```

## See Also
For polygons:
* [SetPolyPt](SetPolyPt.md)

For polylines:
* [GetPolylineVertex](GetPolylineVertex.md)
* [SetPolylineVertex](SetPolylineVertex.md)

## Version
Availability: from All Versions

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
