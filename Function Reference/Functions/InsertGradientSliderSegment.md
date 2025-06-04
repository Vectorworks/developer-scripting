# InsertGradientSliderSegment

## Description
Inserts a new segment into the gradient slider and initializes its data to the specified values.

```pascal
FUNCTION InsertGradientSliderSegment(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				spotPosition : REAL;
				red          : LONGINT;
				green        : LONGINT;
				blue         : LONGINT): INTEGER;
```

```python
def vs.InsertGradientSliderSegment(dialogID, componentID, spotPosition, red, green, blue):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the gradient slider component.|
|componentID|LONGINT|Index to a specific gradient slider component.|
|spotPosition|REAL|Position of the segment's color marker relative to left-most point of the slider. The value should be &gt;= 0.0 and &lt;= 1.0, which represents a percentage distance across the slider.|
|red|LONGINT|Red component of the color spot's color.|(red &gt;= 0 and red &lt;= 255)|
|green|LONGINT|Green component of the color spot's color.|(green &gt;= 0 and green &lt;= 255)|
|blue|LONGINT|Blue component of the color spot's color.|(blue &gt;= 0 and blue &lt;= 255)|

## Examples
==== VectorScript ====
```pascal
segmentIndex := InsertGradientSliderSegment(dialogID, componentID, 0.4, 255, 255, 255);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
