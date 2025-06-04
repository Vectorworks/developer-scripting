# Stipple

## Description
Greates a group of 'stipple-shapes', objects that fill a 'profile object'

```pascal
FUNCTION Stipple(
				hProfileObject : HANDLE;
				shapeType      : INTEGER;
				density        : INTEGER;
				clipToProfile  : INTEGER;
				minSize        : REAL;
				maxSize        : REAL;
				minAspectRatio : REAL;
				maxAspectRatio : REAL;
				randomRotate   : BOOLEAN): HANDLE;
```

```python
def vs.Stipple(hProfileObject, shapeType, density, clipToProfile, minSize, maxSize, minAspectRatio, maxAspectRatio, randomRotate):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hProfileObject|HANDLE|   |
|shapeType|INTEGER|   |
|density|INTEGER|   |
|clipToProfile|INTEGER|   |
|minSize|REAL|   |
|maxSize|REAL|   |
|minAspectRatio|REAL|   |
|maxAspectRatio|REAL|   |
|randomRotate|BOOLEAN|   |

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
