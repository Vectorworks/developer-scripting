# GetTrapeziumAttributes

## Description
Procedure GetTrapeziumAttributes returns the attributes of a trapezium dormer in the referenced roof.

```pascal
PROCEDURE GetTrapeziumAttributes(
				roofObject      : HANDLE;
				dormerID        : INTEGER;
				VAR useHeight   : BOOLEAN;
				VAR heightDepth : REAL;
				VAR bottomWidth : REAL;
				VAR useTopWidth : BOOLEAN;
				VAR topWidth    : REAL;
				VAR leftSlope   : REAL;
				VAR rightSlope  : REAL;
				VAR topSlope    : REAL);
```

```python
def vs.GetTrapeziumAttributes(roofObject, dormerID):
    return (useHeight, heightDepth, bottomWidth, useTopWidth, topWidth, leftSlope, rightSlope, topSlope)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|
|dormerID|INTEGER|Index of dormer element.|
|useHeight|BOOLEAN|Returns if height setting was used to created dormer.|
|heightDepth|REAL|Returns height or depth value.|
|bottomWidth|REAL|Returns bottom width.|
|useTopWidth|BOOLEAN|Returns whether top width was used to create dormer.|
|topWidth|REAL|Returns top width.|
|leftSlope|REAL|Returns left slope of dormer roof.|
|rightSlope|REAL|Returns right slope of dormer roof.|
|topSlope|REAL|Returns top slope of dormer roof.|

## Remarks
This will fail if the dormerID identifies a dormer of a different style, or the dormerID is not valid.

dormerID: Identifies the dormer for which to retrieve the information.

useHeight: true if the next value is the height of the dormer, if false, next value is the depth (front to back) of the dormer.
heightDepthValue: size of the dormer, either by height or depth; determined by previous parameter.

bottomWidth: dimension of bottom front edge of the dormer, left to right.

useTopWidth: true if using a dimension to set the width of the dormer roof.  False if the top width of the dormer is determined by the left and right slope.  The topWidth is exclusive of leftSlope &amp; rightSlope.
twOrLSlope: dimension of the roof of the dormer if previous param is true, or slope of left dormer wall if false.
rightSlope: angle of right dormer wall.
topSlope: angle of the roof of the dormer.

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
