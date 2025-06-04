# InsertGradientData

## Description
A segment consists of a single color spot and the single midpoint immediately to the right of the color spot.

```pascal
FUNCTION InsertGradientData(
				gradient         : HANDLE;
				spotPosition     : REAL;
				midpointPosition : REAL;
				red              : LONGINT;
				green            : LONGINT;
				blue             : LONGINT;
				opacity          : INTEGER): INTEGER;
```

```python
def vs.InsertGradientData(gradient, spotPosition, midpointPosition, red, green, blue, opacity):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient into which a segment is to be inserted.|
|spotPosition|REAL|Position of the segment's color spot relative to left-most point of the gradient.|
|midpointPosition|REAL|Position of the segment's midpoint relative to color spot immediately to left.|
|red|LONGINT|Red component of the color spot's color.|
|green|LONGINT|Green component of the color spot's color.|
|blue|LONGINT|Blue component of the color spot's color.|
|opacity|INTEGER|Opacity of the color spot.|

## Examples
```python
index := InsertGradientData(gradientHandle, 0.35, 0.4, 255, 255, 255, 100);
{ inserts a white color spot at position, 0.35, with a midpoint position of 0.4; 100 is max opacity (i.e. opaque) }
```

## See Also
VS Functions:
[GetGradientDataN](GetGradientDataN.md) 
| [SetGradientDataN](SetGradientDataN.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
