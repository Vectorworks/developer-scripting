# GetShedAttributes

## Description
Procedure GetShedAttributes returns the attributes of a shed dormer in the referenced roof.

```pascal
PROCEDURE GetShedAttributes(
				roofObject      : HANDLE;
				dormerID        : INTEGER;
				VAR useHeight   : BOOLEAN;
				VAR heightDepth : REAL;
				VAR bottomWidth : REAL;
				VAR overhang    : REAL;
				VAR topSlope    : REAL);
```

```python
def vs.GetShedAttributes(roofObject, dormerID):
    return (useHeight, heightDepth, bottomWidth, overhang, topSlope)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|
|dormerID|INTEGER|Index of dormer element.|
|useHeight|BOOLEAN|Returns if height setting was used to created dormer.|
|heightDepth|REAL|Returns height or depth value.|
|bottomWidth|REAL|Returns bottom width.|
|overhang|REAL|Returns overhang distance.|
|topSlope|REAL|Returns top slope of dormer roof.|

## Remarks
This will fail if the dormerID identifies a dormer of a different style, or the dormerID is not valid.

dormerID: Identifies the dormer for which to retrieve the information.

useHeight: Set to true if the next value is the height of the dormer, if false, next value is the depth (front to back) of the dormer.
heightDepthValue: Size of the dormer, either by height or depth; determined by previous parameter.

bottomWidth: Dimension of bottom front edge of the dormer, left to right.

topSlope: Angle of dormer roof.

overhang: Distance roof projects past dormer walls.

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
