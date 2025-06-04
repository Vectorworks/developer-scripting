# InsertGradientSliSeg

```pascal
FUNCTION InsertGradientSliSeg(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				spotPosition : REAL;
				red          : LONGINT;
				green        : LONGINT;
				blue         : LONGINT;
				opacity      : INTEGER): INTEGER;
```

```python
def vs.InsertGradientSliSeg(dialogID, componentID, spotPosition, red, green, blue, opacity):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the gradient slider component.|
|componentID|LONGINT|Index to a specific gradient slider component.|
|spotPosition|REAL|Position of the segment's color marker relative to left-most point of the slider. The value should be &gt;= 0.0 and &lt;= 1.0, which represents a percentage distance across the slider.|
|red|LONGINT|Red component of the color spot's color.|
|green|LONGINT|Green component of the color spot's color.|
|blue|LONGINT|Blue component of the color spot's color.|
|opacity|INTEGER|Opacity for the color at the spot position.|

## Examples
```python
segmentIndex := InsertGradientSliSeg(dialogID, componentID, 0.4, 255, 255, 255, 100);
```

## See Also
VS Functions:
[GetGradientSlider](GetGradientSlider.md) 
| [SetGradientSlider](SetGradientSlider.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
