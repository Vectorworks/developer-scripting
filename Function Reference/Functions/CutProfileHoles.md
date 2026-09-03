# CutProfileHoles

## Description
Cut holes in object geometry described in it's profile group.

```pascal
PROCEDURE CutProfileHoles(hWall : HANDLE);
```

```python
def vs.CutProfileHoles(hWall):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hWall|HANDLE|   |

## Examples
```pascal
CutProfileHoles(hWall);
```
```python
import vs

# Cut holes in object geometry described in it's profile group.
hWall = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.CutProfileHoles(hWall)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
