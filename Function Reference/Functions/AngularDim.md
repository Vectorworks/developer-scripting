# AngularDim

## Description
Procedure AngularDim creates an angular dimension in the document.

Bit code values for dimension flags can be found in the [[VS:Function Reference Appendix#LinearDim|VectorScript Appendix]].


*Angular Dimension

[[Image:angdim.gif]]

```pascal
PROCEDURE AngularDim(
				startPtX,startPtY  : REAL;
				endPtX,endPtY      : REAL;
				vert1X,vert1Y      : REAL;
				textOffsetDistance : REAL;
				arrow              : INTEGER;
				textFlag           : INTEGER;
				posAngle           : REAL);
```

```python
def vs.AngularDim(startPt, endPt, vert1, textOffsetDistance, arrow, textFlag, posAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|startPt|REAL|X-Y coordinates of dimension start point.|
|endPt|REAL|X-Y coordinates of dimension end point|
|vert1|REAL|X-Y coordinates of dimension arc center.|
|textOffsetDistance|REAL|Offset from dimension arc center (radius of the dimension arc).|
|arrow|INTEGER|Dimension arrowhead style flag.|
|textFlag|INTEGER|Dimension text style flag.|
|posAngle|REAL|Position angle of dimension text(from start). Auto position text overrides this value.|

## Examples
#### VectorScript ####
```pascal
AngularDim(1 1/2&quot;,3/8&quot;,-1/4&quot;,-1/2&quot;,7/8&quot;,-1/2&quot;,1.7001838&quot;,771,770,#35d 32'16&quot;);
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Dimensions](../Categories/Dimensions.md)
