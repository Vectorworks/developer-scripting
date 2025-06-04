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

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
