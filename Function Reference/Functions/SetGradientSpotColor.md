# SetGradientSpotColor

## Description
Sets the spot color of the specified gradient segment.

```pascal
PROCEDURE SetGradientSpotColor(
				gradient     : HANDLE;
				segmentIndex : INTEGER;
				red          : LONGINT;
				green        : LONGINT;
				blue         : LONGINT);
```

```python
def vs.SetGradientSpotColor(gradient, segmentIndex, red, green, blue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient that contains the segment.|
|segmentIndex|INTEGER|Segment for which to set the data.|(segment indexes begin with 1)|
|red|LONGINT|Red component of the color spot's color.|(red &gt;= 0 and red &lt;= 255)|
|green|LONGINT|Green component of the color spot's color.|(green &gt;= 0 and green &lt;= 255)|
|blue|LONGINT|Blue component of the color spot's color.|(blue &gt;= 0 and blue &lt;= 255)|

## Examples
#### VectorScript ####
```pascal
SetGradientSpotColor(gradientHandle, 4, 255, 255, 255);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
