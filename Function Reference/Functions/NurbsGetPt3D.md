# NurbsGetPt3D

## Description
Returns the coordinates of a point in the referenced NURBS curve or surface.

The index is zero based (0 to number of points - 1).

```pascal
PROCEDURE NurbsGetPt3D(
				objectHd     : HANDLE;
				index1       : LONGINT;
				index2       : LONGINT;
				VAR pX,pY,pZ : REAL);
```

```python
def vs.NurbsGetPt3D(objectHd, index1, index2):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to NURBS curve or surface.|
|index1|LONGINT|Index of point in NURBS curve, or u-coordinate of point location in NURBS surface.|
|index2|LONGINT|V-coordinate of point location in NURBS surface.|
|p|REAL|Coordinates of the control point.|

## Remarks
this function will work for both nurbs curves and nurbs surfaces. 

Gets the index2 vertex of the indexe1 piece of the given NURBS curve or the index1 U and index2 V control point of the surfaces.

For a nurbs curve, index1 is the piece number of the nurbs curve. Index2 is the vertex number within that piece.

NurbsCurveGetNumPieces will give you the number of pieces inside of the nurbs curve. (1-based)

NurbsGetNumPts will give you the number of points inside of a piece.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
    nurbsObj : HANDLE;
    segm, segmentCnt, vtx, vtxCnt : LONGINT;
    v : VECTOR;

BEGIN
    { take care to select a NURBS Curve }
    nurbsObj := FSActLayer;
	
    { pieces are segments, you need pieces to realize edgy NURBS, appearing as corner pt edges }
    segmentCnt := NurbsCurveGetNumPieces(nurbsObj);
   
    segm := 0;
    WHILE segm < segmentCnt DO BEGIN
        vtxCnt := NurbsGetNumPts(nurbsObj, segm);
        
        vtx := 0;
        WHILE vtx < vtxCnt DO BEGIN
            NurbsGetPt3D(nurbsObj, segm, vtx, v.x, v.y, v.z);
			
            MoveTo(v.x, v.y);
            CreateText(Concat(segm, '.', vtx));
            vtx := vtx +1;
        END;
        segm := segm +1;
    END;
END;
Run(Example);
```
#### Python ####
```python
nurbsObj = vs.FSActLayer() # take care to select a NURBS curve

# pieces are segments, you need pieces to realize edgy NURBS, appearing as corner pt edges
segmentCnt = vs.NurbsCurveGetNumPieces(nurbsObj) 
for segm in range(0, segmentCnt): # python range is always one less than pascal
	
	vtxCnt = vs.NurbsGetNumPts(nurbsObj, segm)
	for vtx in range(0, vtxCnt): # python range is always one less than pascal
		v = vs.NurbsGetPt3D(nurbsObj, segm, vtx)
		
		vs.MoveTo(v)
		vs.CreateText(f'{segm}.{vtx}')
```
VectorScript ====
```pascal
PROCEDURE Example;
VAR
    nurbsObj : HANDLE;
    segm, segmentCnt, vtx, vtxCnt : LONGINT;
    v : VECTOR;

BEGIN
    { take care to select a NURBS Curve }
    nurbsObj := FSActLayer;
	
    { pieces are segments, you need pieces to realize edgy NURBS, appearing as corner pt edges }
    segmentCnt := NurbsCurveGetNumPieces(nurbsObj);
   
    segm := 0;
    WHILE segm < segmentCnt DO BEGIN
        vtxCnt := NurbsGetNumPts(nurbsObj, segm);
        
        vtx := 0;
        WHILE vtx < vtxCnt DO BEGIN
            NurbsGetPt3D(nurbsObj, segm, vtx, v.x, v.y, v.z);
			
            MoveTo(v.x, v.y);
            CreateText(Concat(segm, '.', vtx));
            vtx := vtx +1;
        END;
        segm := segm +1;
    END;
END;
Run(Example);
```

#### Python ####
```python
nurbsObj = vs.FSActLayer() # take care to select a NURBS curve

# pieces are segments, you need pieces to realize edgy NURBS, appearing as corner pt edges
segmentCnt = vs.NurbsCurveGetNumPieces(nurbsObj) 
for segm in range(0, segmentCnt): # python range is always one less than pascal
	
	vtxCnt = vs.NurbsGetNumPts(nurbsObj, segm)
	for vtx in range(0, vtxCnt): # python range is always one less than pascal
		v = vs.NurbsGetPt3D(nurbsObj, segm, vtx)
		
		vs.MoveTo(v)
		vs.CreateText(f'{segm}.{vtx}')
```

A representation of pieces (segments in the example) in a NURBS curve:

![NURBS_Pieces.png](files/NURBS_Pieces.png)

## See Also
VS Functions:
[NurbsCurveEvalPt](NurbsCurveEvalPt.md) 
| [NurbsSurfaceEvalPt](NurbsSurfaceEvalPt.md)

## Version
Availability: from VectorWorks 9.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
