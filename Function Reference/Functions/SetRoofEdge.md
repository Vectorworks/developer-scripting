# SetRoofEdge

## Description
Procedure SetRoofEdge sets the definition attributes of a roof edge for the referenced roof object.

```pascal
PROCEDURE SetRoofEdge(
				roofObject          : HANDLE;
				index               : INTEGER;
				vertexPtX,vertexPtY : REAL;
				edgeAngle           : REAL;
				projectionDistance  : REAL;
				eaveHeightDistance  : REAL);
```

```python
def vs.SetRoofEdge(roofObject, index, vertexPt, edgeAngle, projectionDistance, eaveHeightDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|
|index|INTEGER|Index of roof edge.|
|vertexPt|REAL|Coordinates of roof edge vertex.|
|edgeAngle|REAL|Roof slope.|
|projectionDistance|REAL|Eave overhang.|
|eaveHeightDistance|REAL|Eave height.|

## Remarks
Vertices define the outline of the roof and its characteristics.  Vertices must progress in a counter clock wise direction, when viewed from a top view, otherwise the roof cannot be built.

index: Indexs have values between 1 and NVertices (See GetRoofVertices())
edgePt: Coordinate point for this edge
slope: pitch of this roof edge
projection: eave overhang
eaveHeight: eave height

## Examples
```pascal
SetRoofEdge(roofObject, 1, 1.0, 2.0, 0.5, 1.5, 3.0);
```
```python
import vs

# Procedure SetRoofEdge sets the definition attributes of a roof edge for the
# referenced roof object.
roofObject = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1
vertexPt = (0, 0)
edgeAngle = 45.0
projectionDistance = 1.0
eaveHeightDistance = 2.0

vs.SetRoofEdge(roofObject, index, vertexPt, edgeAngle, projectionDistance, eaveHeightDistance)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
