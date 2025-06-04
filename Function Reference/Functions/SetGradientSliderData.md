# SetGradientSliderData

## Description
Sets the spot position, midpoint position and color of the specified gradient slider segment.

Note: you must use a variable, initialized to the segment index, to pass as a parameter. After the data has been set, this variable will contain the index of the segment, which may have changed because of the spot position specified.

```pascal
PROCEDURE SetGradientSliderData(
				dialogID         : LONGINT;
				componentID      : LONGINT;
				VAR segmentIndex : INTEGER;
				spotPosition     : REAL;
				midpointPosition : REAL;
				red              : LONGINT;
				green            : LONGINT;
				blue             : LONGINT);
```

```python
def vs.SetGradientSliderData(dialogID, componentID, segmentIndex, spotPosition, midpointPosition, red, green, blue):
    return segmentIndex
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the gradient slider component.|
|componentID|LONGINT|Index to a specific gradient slider component.|
|segmentIndex|INTEGER|Segment for which to set the data.|(segment indexes begin with 1)|
|spotPosition|REAL|Position of the segment's color marker relative to left-most point of the slider.|(position &gt;= 0.0 and position &lt;= 1.0)|
|midpointPosition|REAL|Position of the segment's midpoint marker relative to color marker immediately to left.|(position &gt;= 0.0 and position &lt;= 1.0)|
|red|LONGINT|Red component of the color spot's color.|(red &gt;= 0 and red &lt;= 255)|
|green|LONGINT|Green component of the color spot's color.|(green &gt;= 0 and green &lt;= 255)|
|blue|LONGINT|Blue component of the color spot's color.|(blue &gt;= 0 and blue &lt;= 255)|

## Examples
#### VectorScript ####
```pascal
segmentIndex := 4;
SetGradientSliderData(dialogID, componentID, segmentIndex, 0.9, 0.5, 255, 255, 255);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
