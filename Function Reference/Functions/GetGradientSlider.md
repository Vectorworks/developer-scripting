# GetGradientSlider

```pascal
PROCEDURE GetGradientSlider(
				dialogID             : LONGINT;
				componentID          : LONGINT;
				segmentIndex         : INTEGER;
				VAR spotPosition     : REAL;
				VAR midpointPosition : REAL;
				VAR red              : LONGINT;
				VAR green            : LONGINT;
				VAR blue             : LONGINT;
				VAR opacity          : INTEGER);
```

```python
def vs.GetGradientSlider(dialogID, componentID, segmentIndex):
    return (spotPosition, midpointPosition, red, green, blue, opacity)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the gradient slider component.|
|componentID|LONGINT|Index to a specific gradient slider component.|
|segmentIndex|INTEGER|Segment from which to get the data.|
|spotPosition|REAL|Position of the segment's color marker relative to left-most point of the slider.|
|midpointPosition|REAL|Position of the segment's midpoint marker relative to color marker immediately to left.|
|red|LONGINT|Red component of the color spot's color.|
|green|LONGINT|Red component of the color spot's color.|
|blue|LONGINT|Blue component of the color spot's color.|
|opacity|INTEGER|Opacity for the color at the spot position.|

## Examples
```python
GetGradientSlider(dialogID, componentID, 4, spotPosition, midpointPosition, red, green, blue,opacity);
```

## See Also
VS Functions:
[SetGradientSlider](SetGradientSlider.md) 
| [InsertGradientSliSeg](InsertGradientSliSeg.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
