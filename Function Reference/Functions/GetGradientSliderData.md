# GetGradientSliderData

## Description
Gets the spot position, midpoint position and color of the specified gradient slider segment.

```pascal
PROCEDURE GetGradientSliderData(
				dialogID             : LONGINT;
				componentID          : LONGINT;
				segmentIndex         : INTEGER;
				VAR spotPosition     : REAL;
				VAR midpointPosition : REAL;
				VAR red              : LONGINT;
				VAR green            : LONGINT;
				VAR blue             : LONGINT);
```

```python
def vs.GetGradientSliderData(dialogID, componentID, segmentIndex):
    return (spotPosition, midpointPosition, red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the gradient slider component.|
|componentID|LONGINT|Index to a specific gradient slider component.|
|segmentIndex|INTEGER|Segment from which to get the data.|(segment indexes begin with 1)|
|spotPosition|REAL|Position of the segment's color marker relative to left-most point of the slider.|(position >= 0.0 and position <= 1.0)|
|midpointPosition|REAL|Position of the segment's midpoint marker relative to color marker immediately to left.|(position >= 0.0 and position <= 1.0)|
|red|LONGINT|Red component of the color spot's color.|(red >= 0 and red <= 255)|
|green|LONGINT|Green component of the color spot's color.|(green >= 0 and green <= 255)|
|blue|LONGINT|Blue component of the color spot's color.|(blue >= 0 and blue <= 255)|

## Examples
#### VectorScript ####
```pascal
GetGradientSliderData(dialogID, componentID, 4, 0.7, 0.3, 255, 255, 255);
```
#### Python ####
```python
vs.GetGradientSliderData(dialogID, componentID, 4)
```

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
