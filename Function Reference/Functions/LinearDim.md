# LinearDim

## Description
Procedure LinearDim creates a linear dimension in a VectorWorks document.

Bit code values for dimension flags can be found in the [[VS:Function Reference Appendix#LinearDim|VectorScript Appendix]].

[[Image:lindim.gif|Linear Dimension]]


October 30, 2023 Pat Stanford
The image above is incorrect. The Offset shown in the image is not the offset that actually occurs in the function. The Offset value that is actually used in the function appears to be the offset of the text along the dimension line, specified in Page units. There is no option of the LinearDim function that will change the offset of the text away from the Dimension line.

If you need to change the text offset, you need to use SetObjectVariableReal with an index of 43 followed by a ResetObject.  Something Like:

::LinearDim(-2",2",1",2",-3",0,771,770,0.75);
::SetObjectVariableReal(LNewObj,43,0); {0 for the value centers the text on the Dimension line}
::ResetObject(LNewObj);

```pascal
PROCEDURE LinearDim(
				startPtX,startPtY : REAL;
				endPtX,endPtY     : REAL;
				offsetDistance    : REAL;
				dimType           : INTEGER;
				arrow             : INTEGER;
				textFlag          : INTEGER;
				textOffset        : REAL);
```

```python
def vs.LinearDim(startPt, endPt, offsetDistance, dimType, arrow, textFlag, textOffset):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|startPt|REAL|X-Y coordinates of dimension start point.|
|endPt|REAL|X-Y coordinates of dimension end point.|
|offsetDistance|REAL|Offset distance of dimension line from object.|
|dimType|INTEGER|Dimension type flag.|
|arrow|INTEGER|Arrowhead style flag.|
|textFlag|INTEGER|Text style flag.|
|textOffset|REAL|Dimension text offset distance.|

## Examples
==== VectorScript ====
```pascal
LinearDim(-2&quot;,2&quot;,1&quot;,2&quot;,-3&quot;,0,771,770,0.75);
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Dimensions](../Categories/Dimensions.md)
