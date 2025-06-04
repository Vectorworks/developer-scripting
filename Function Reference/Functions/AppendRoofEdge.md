# AppendRoofEdge

## Description
Function AppendRoofEdge creates a new edge in the referenced roof object.

```pascal
PROCEDURE AppendRoofEdge(
				theRoof            : HANDLE;
				edgePtX,edgePtY    : REAL;
				slopeAngle         : REAL;
				projectionDistance : REAL;
				eaveHeightDistance : REAL);
```

```python
def vs.AppendRoofEdge(theRoof, edgePt, slopeAngle, projectionDistance, eaveHeightDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theRoof|HANDLE|Handle to roof.|
|edgePt|REAL|Definition point of roof edge.|
|slopeAngle|REAL|Slope of roof edge.|
|projectionDistance|REAL|Eave overhang.|
|eaveHeightDistance|REAL|Eave height.|

## Remarks
Vertex is appended to the end of the list of vertices.  Vertices define the outline of the roof.  Vertices must progress in a counter clock wise direction, when viewed from a top view, otherwise the roof cannot be built.

edgePt: Coordinate point for this edge
slope: pitch of this roof edge
projection: eave overhang
eaveHeight: eave height

## Examples
eateRoofObj}}

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
