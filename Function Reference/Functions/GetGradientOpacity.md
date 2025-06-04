# GetGradientOpacity

```pascal
PROCEDURE GetGradientOpacity(
				gradient     : HANDLE;
				segmentIndex : INTEGER;
				VAR opacity  : INTEGER);
```

```python
def vs.GetGradientOpacity(gradient, segmentIndex):
    return opacity
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient that contains the segment.|
|segmentIndex|INTEGER|Segment from which to get the data.|
|opacity|INTEGER|Opacity at the spot position.|

## Examples
```python
GetGradientOpacity(gradientHandle, 4, opacity);
```

## See Also
VS Functions:
[SetGradientOpacity](SetGradientOpacity.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
