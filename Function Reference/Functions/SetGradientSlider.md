# SetGradientSlider

## Description
Note: you must use a variable, initialized to the segment index, to pass as a parameter. After the data has been set, this variable will contain the index of the segment, which may have changed because of the spot position specified.

```pascal
PROCEDURE SetGradientSlider(
				dialogID         : LONGINT;
				componentID      : LONGINT;
				VAR segmentIndex : INTEGER;
				spotPosition     : REAL;
				midpointPosition : REAL;
				red              : LONGINT;
				green            : LONGINT;
				blue             : LONGINT;
				opacity          : INTEGER);
```

```python
def vs.SetGradientSlider(dialogID, componentID, segmentIndex, spotPosition, midpointPosition, red, green, blue, opacity):
    return segmentIndex
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the gradient slider component.|
|componentID|LONGINT|Index to a specific gradient slider component.|
|segmentIndex|INTEGER|Segment for which to set the data.|
|spotPosition|REAL|Position of the segment's color marker relative to left-most point of the slider.|
|midpointPosition|REAL|Position of the segment's midpoint marker relative to color marker immediately to left.|
|red|LONGINT|Red component of the color spot's color.|
|green|LONGINT|Green component of the color spot's color.|
|blue|LONGINT|Blue component of the color spot's color.|
|opacity|INTEGER|Opacity for the color at the spot position.|

## Examples
```python
segmentIndex := 4;
SetGradientSlider(dialogID, componentID, segmentIndex, 0.9, 0.5, 255, 255, 255,100);
```

## See Also
VS Functions:
[GetGradientSlider](GetGradientSlider.md) 
| [InsertGradientSliSeg](InsertGradientSliSeg.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
