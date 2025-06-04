# GetRoofEdge

## Description
Procedure GetRoofEdge returns the definition attributes of a roof edge for the referenced roof object.

```pascal
FUNCTION GetRoofEdge(
				theRoof                 : HANDLE;
				index                   : INTEGER;
				VAR vertexPtX,vertexPtY : REAL;
				VAR slope               : REAL;
				VAR projection          : REAL;
				VAR eaveHeight          : REAL): BOOLEAN;
```

```python
def vs.GetRoofEdge(theRoof, index):
    return (BOOLEAN, vertexPt, slope, projection, eaveHeight)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theRoof|HANDLE|Handle to roof.|
|index|INTEGER|Index of roof edge (in a range of 1 - n).|
|vertexPt|REAL|Returns coordinates of roof edge definition vertex.|
|slope|REAL|Returns slope of roof edge.|
|projection|REAL|Retunrs eave overhang dimension.|
|eaveHeight|REAL|Returns eave height.|

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
