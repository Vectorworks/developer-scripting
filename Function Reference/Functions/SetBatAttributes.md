# SetBatAttributes

## Description
Procedure SetBatAttributes sets the attributes of a bat dormer in the referenced roof.

```pascal
PROCEDURE SetBatAttributes(
				roofObject               : HANDLE;
				dormerID                 : INTEGER;
				useHeight                : BOOLEAN;
				heightDepthValueDistance : REAL;
				bottomWidthDistance      : REAL;
				topWidthDistance         : REAL;
				baseHeightDistance       : REAL;
				controlPointDistance     : REAL;
				topAngle                 : REAL);
```

```python
def vs.SetBatAttributes(roofObject, dormerID, useHeight, heightDepthValueDistance, bottomWidthDistance, topWidthDistance, baseHeightDistance, controlPointDistance, topAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roofObject|HANDLE|Handle to roof.|
|dormerID|INTEGER|Index of dormer element.|
|useHeight|BOOLEAN|Use height setting to create dormer element.|
|heightDepthValueDistance|REAL|Height/depth distance.|
|bottomWidthDistance|REAL|Bottom width.|
|topWidthDistance|REAL|Top width.|
|baseHeightDistance|REAL|Base height of bat.|
|controlPointDistance|REAL|Offset distance of control point.|
|topAngle|REAL|Slope of bat roof.|

## Remarks
dormerID: Identifies the dormer for which to set the information.

useHeight: Set to true if the next value is the height of the dormer, if false, next value is the depth (front to back) of the dormer.
heightDepthValue: Size of the dormer, either by height or depth; determined by previous parameter.

bottomWidth: Dimension of bottom front edge of the dormer, left to right..
topWidth: Dimension of the roof of the dormer.
baseHeight: Dimension of the bottom half of the dormer.

topSlope: Angle of the dormer roof.

controlPoint: The distance from the side to where the curve starts.  Must be less than (bottomWidth - topWidth) / 2.

## Examples
#### VectorScript ####
```pascal
roofHandle := CreateRoof(TRUE,5 1/2&quot;,5 1/2&quot;,4,9.52627&quot;);
AppendRoofEdge(roofHandle,-77'10&quot;,-25'3.18078&quot;,#45&quot;,2'0&quot;,10'0&quot;);
AppendRoofEdge(roofHandle,-41'2&quot;,-25'3.18078&quot;,#45&quot;,2'0&quot;,10'0&quot;);
AppendRoofEdge(roofHandle,-41'2&quot;,21'4.81922&quot;,#45&quot;,2'0&quot;,10'0&quot;);
AppendRoofEdge(roofHandle,-77'10&quot;,21'4.81922&quot;,#45&quot;,2'0&quot;,10'0&quot;);
batID := CreateBatDormer(roofHandle);
SetBatAttributes(roofHandle,batID,TRUE,5'0&quot;,10'0&quot;,4'0&quot;,6'3&quot;,2'0&quot;,#8&quot;);
SetDormerAttributes(roofHandle,batID,3,18'4&quot;,TRUE,3'0&quot;,63,FALSE,3'0&quot;);
SetDormerThick(roofHandle, 2&quot;,1.83333&quot;);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
