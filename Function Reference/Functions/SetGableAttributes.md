# SetGableAttributes

## Description
Procedure SetGableAttributes sets the attributes of a gable dormer in the referenced roof.

```pascal
PROCEDURE SetGableAttributes(
				roofObject          : HANDLE;
				dormerID            : INTEGER;
				useHeight           : BOOLEAN;
				heightDepthDistance : REAL;
				bottomWidthDistance : REAL;
				overhangDistance    : REAL;
				leftAngle           : REAL;
				rightAngle          : REAL);
```

```python
def vs.SetGableAttributes(roofObject, dormerID, useHeight, heightDepthDistance, bottomWidthDistance, overhangDistance, leftAngle, rightAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|
|dormerID|INTEGER|Index of dormer element.|
|useHeight|BOOLEAN|Use height setting to create dormer element.|
|heightDepthDistance|REAL|Height/depth distance.|
|bottomWidthDistance|REAL|Bottom width.|
|overhangDistance|REAL|Overhang distance.|
|leftAngle|REAL|Slope of left roof.|
|rightAngle|REAL|Slope of right roof.|

## Remarks
dormerID: Identifies the dormer for which to set the information.

useHeight: Set to true if the next value is the height of the dormer, if false, next value is the depth (front to back) of the dormer.
heightDepthValue: Size of the dormer, either by height or depth; determined by previous parameter.

bottomWidth: Dimension of bottom front edge of the dormer, left to right.

leftSlope: Angle of left dormer roof.
rightSlope: Angle of right dormer roof.

overhang: Distance roof projects past dormer walls.

## Examples
[CreateRoofOb](examples/CreateRoofObj.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
