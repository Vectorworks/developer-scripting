# SetGradientOpacity

```pascal
PROCEDURE SetGradientOpacity(
				gradient     : HANDLE;
				segmentIndex : INTEGER;
				opacity      : INTEGER);
```

```python
def vs.SetGradientOpacity(gradient, segmentIndex, opacity):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|gradient|HANDLE|Gradient that contains the segment.|
|segmentIndex|INTEGER|Segment for which to set the data.|
|opacity|INTEGER|Opacity at the spot position.|

## Examples
```python
SetGradientSpotColor(gradientHandle, 4, 100);
```

```pascal
SetGradientOpacity(gradient, 1, 2);
```
```python
import vs

gradient = vs.FSActLayer()  # handle to the first selected object on the active layer
segmentIndex = 1
opacity = 1

vs.SetGradientOpacity(gradient, segmentIndex, opacity)
```

## See Also
VS Functions:
[GetGradientOpacity](GetGradientOpacity.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
