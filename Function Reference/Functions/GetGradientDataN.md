# GetGradientDataN

```pascal
PROCEDURE GetGradientDataN(
				gradient             : HANDLE;
				segmentIndex         : INTEGER;
				VAR spotPosition     : REAL;
				VAR midpointPosition : REAL;
				VAR red              : LONGINT;
				VAR green            : LONGINT;
				VAR blue             : LONGINT;
				VAR opacity          : INTEGER);
```

```python
def vs.GetGradientDataN(gradient, segmentIndex):
    return (Boolean, spotPosition, midpointPosition, red, green, blue, opacity)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient that contains the segment.|
|segmentIndex|INTEGER|Segment from which to get the data.|
|spotPosition|REAL|Position of the segment's color spot relative to left-most point of the gradient.|
|midpointPosition|REAL|Position of the segment's midpoint relative to color spot immediately to left.|
|red|LONGINT|Red component of the color spot's color.|
|green|LONGINT|Green component of the color spot's color.|
|blue|LONGINT|Blue component of the color spot's color.|
|opacity|INTEGER|Opacity of the color spot.|

## Examples
```python
PROCEDURE Example;
VAR
gradient :HANDLE;
segmentIndex :INTEGER;
spotPosition, midpointPosition :REAL;
red, green, blue :LONGINT;
opacity :INTEGER
BEGIN
gradient := GetObject('Cyan-Magenta-Yellow');
segmentIndex := 3;
GetGradientData(gradient, segmentIndex, spotPosition, midpointPosition, red, green, blue.opacity);
Message(red, ' ', green, ' ', blue, ' ', opacity);
END;
RUN(Example);
```

## See Also
VS Functions:
[SetGradientDataN](SetGradientDataN.md) 
| [InsertGradientData](InsertGradientData.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
