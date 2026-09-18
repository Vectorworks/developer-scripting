# GetPtInPoly

## Description
Finds a point inside a polyline.

```pascal
FUNCTION GetPtInPoly(h : HANDLE): VECTOR;
```

```python
def vs.GetPtInPoly(h):
    return VECTOR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |

## Examples
```pascal
result := GetPtInPoly(h);
```
```python
import vs

# Finds a point inside a polyline.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

vec = vs.GetPtInPoly(h)
vs.Message('GetPtInPoly returned: ' + str(vec))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
