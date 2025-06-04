# GetGradientSpotColor

## Description
Gets the spot color of the specified gradient segment.

```pascal
PROCEDURE GetGradientSpotColor(
				gradient     : HANDLE;
				segmentIndex : INTEGER;
				VAR red      : LONGINT;
				VAR green    : LONGINT;
				VAR blue     : LONGINT);
```

```python
def vs.GetGradientSpotColor(gradient, segmentIndex):
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient that contains the segment.|
|segmentIndex|INTEGER|Segment from which to get the data.|(segment indexes begin with 1)|
|red|LONGINT|Red component of the color spot's color.|(red &gt;= 0 and red &lt;= 255)|
|green|LONGINT|Green component of the color spot's color.|(green &gt;= 0 and green &lt;= 255)|
|blue|LONGINT|Blue component of the color spot's color.|(blue &gt;= 0 and blue &lt;= 255)|

## Examples
==== VectorScript ====
```pascal
GetGradientSpotColor(gradientHandle, 4, red, green, blue);
```
==== Python ====
```python
red, green, blue = vs.GetGradientSpotColor(gradientHandle, 4)
```

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
