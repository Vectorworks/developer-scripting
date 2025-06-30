# SetGradientData

## Description
Sets the spot position, midpoint position and color of the specified gradient segment.

Note: you must use a variable, initialized to the segment index, to pass as a parameter. After the data has been set, this variable will contain the index of the segment, which may have changed because of the spot position specified.

```pascal
PROCEDURE SetGradientData(
				gradient         : HANDLE;
				VAR segmentIndex : INTEGER;
				spotPosition     : REAL;
				midpointPosition : REAL;
				red              : LONGINT;
				green            : LONGINT;
				blue             : LONGINT);
```

```python
def vs.SetGradientData(gradient, segmentIndex, spotPosition, midpointPosition, red, green, blue):
    return segmentIndex
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient that contains the segment.|
|segmentIndex|INTEGER|Segment for which to set the data.|(segment indexes begin with 1)|
|spotPosition|REAL|Position of the segment's color spot relative to left-most point of the gradient.|(position >= 0.0 and position <= 1.0)|
|midpointPosition|REAL|Position of the segment's midpoint relative to color spot immediately to left.|(position >= 0.0 and position <= 1.0)|
|red|LONGINT|Red component of the color spot's color.|(red >= 0 and red <= 255)|
|green|LONGINT|Green component of the color spot's color.|(green >= 0 and green <= 255)|
|blue|LONGINT|Blue component of the color spot's color.|(blue >= 0 and blue <= 255)|

## Examples
#### VectorScript ####
```pascal
segmentIndex := 4;
SetGradientData(gradientHandle, segmentIndex, 0.9, 0.5, 255, 255, 255);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
