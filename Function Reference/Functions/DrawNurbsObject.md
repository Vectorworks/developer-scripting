# DrawNurbsObject

## Description
Draws the NURBS object h on the screen.

```pascal
PROCEDURE DrawNurbsObject(h : HANDLE);
```

```python
def vs.DrawNurbsObject(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |

## Examples
```pascal
DrawNurbsObject(h);
```
```python
import vs

# Draws the NURBS object h on the screen.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.DrawNurbsObject(h)
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
