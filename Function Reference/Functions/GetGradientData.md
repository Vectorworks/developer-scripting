# GetGradientData

## Description
Gets the spot position, midpoint position and color of the specified gradient segment.

```pascal
PROCEDURE GetGradientData(
				gradient             : HANDLE;
				segmentIndex         : INTEGER;
				VAR spotPosition     : REAL;
				VAR midpointPosition : REAL;
				VAR red              : LONGINT;
				VAR green            : LONGINT;
				VAR blue             : LONGINT);
```

```python
def vs.GetGradientData(gradient, segmentIndex):
    return (spotPosition, midpointPosition, red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient that contains the segment.|
|segmentIndex|INTEGER|Segment from which to get the data.|(segment indexes begin with 1)|
|spotPosition|REAL|Position of the segment's color spot relative to left-most point of the gradient.|(position >= 0.0 and position <= 1.0)|
|midpointPosition|REAL|Position of the segment's midpoint relative to color spot immediately to left.|(position >= 0.0 and position <= 1.0)|
|red|LONGINT|Red component of the color spot's color.|(red >= 0 and red <= 255)|
|green|LONGINT|Green component of the color spot's color.|(green >= 0 and green <= 255)|
|blue|LONGINT|Blue component of the color spot's color.|(blue >= 0 and blue <= 255)|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
gradient :HANDLE;
segmentIndex :INTEGER;
spotPosition, midpointPosition :REAL;
red, green, blue :LONGINT;
BEGIN
gradient := GetObject('Cyan-Magenta-Yellow');
segmentIndex := 3;
if gradient <> NIL then
Begin  
GetGradientData(gradient, segmentIndex, spotPosition, midpointPosition, red, green, blue);
Message(red, ' ', green, ' ', blue);
END;
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	gradient = vs.GetObject('Cyan-Magenta-Yellow')
	segmentIndex = 3
	if gradient != None:
		spotPosition, midpointPosition, red, green, blue = vs.GetGradientData(gradient, segmentIndex)
		vs.Message(red, ' ', green, ' ', blue)
Example()
```

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
