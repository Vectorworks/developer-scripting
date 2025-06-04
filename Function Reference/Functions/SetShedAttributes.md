# SetShedAttributes

## Description
Procedure SetShedAttributes sets the attributes of a shed dormer in the referenced roof.

```pascal
PROCEDURE SetShedAttributes(
				roofObject          : HANDLE;
				dormerID            : INTEGER;
				useHeight           : BOOLEAN;
				heightDepthDistance : REAL;
				bottomWidthDistance : REAL;
				overhangDistance    : REAL;
				topAngle            : REAL);
```

```python
def vs.SetShedAttributes(roofObject, dormerID, useHeight, heightDepthDistance, bottomWidthDistance, overhangDistance, topAngle):
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
|topAngle|REAL|Top angle of dormer element.|

## Remarks
dormerID: Identifies the dormer for which to set the information.

useHeight: true if the next value is the height of the dormer, if false, next value is the depth (front to back) of the dormer
heightDepthValue: size of the dormer, either by height or depth; determined by previous parameter.

bottomWidth: Dimension of bottom front edge of the dormer, left to right.

topSlope: Angle of dormer roof.

overhang: Distance roof projects past dormer walls.

## Examples
eateShedDormer}}

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
