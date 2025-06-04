# SetGradientDataN

## Description
Note: you must use a variable, initialized to the segment index, to pass as a parameter. After the data has been set, this variable will contain the index of the segment, which may have changed because of the spot position specified.

```pascal
PROCEDURE SetGradientDataN(
				gradient         : HANDLE;
				VAR segmentIndex : INTEGER;
				spotPosition     : REAL;
				midpointPosition : REAL;
				red              : LONGINT;
				green            : LONGINT;
				blue             : LONGINT;
				opacity          : INTEGER);
```

```python
def vs.SetGradientDataN(gradient, segmentIndex, spotPosition, midpointPosition, red, green, blue, opacity):
    return segmentIndex
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient that contains the segment.|
|segmentIndex|INTEGER|Segment for which to set the data.|
|spotPosition|REAL|Position of the segment's color spot relative to left-most point of the gradient.|
|midpointPosition|REAL|Position of the segment's midpoint relative to color spot immediately to left.|
|red|LONGINT|Red component of the color spot's color.|
|green|LONGINT|Green component of the color spot's color.|
|blue|LONGINT|Blue component of the color spot's color.|
|opacity|INTEGER|Opacity of the color spot.|

## Examples
```python
segmentIndex := 4;
SetGradientData(gradientHandle, segmentIndex, 0.9, 0.5, 255, 255, 255,100);
```

## See Also
VS Functions:
[GetGradientDataN](GetGradientDataN.md) 
| [InsertGradientData](InsertGradientData.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
