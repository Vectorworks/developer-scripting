# SetRRDiam

## Description
Sets the diameters of a rounded rectangle.

```pascal
PROCEDURE SetRRDiam(
				h     : HANDLE;
				xDiam : REAL;
				yDiam : REAL);
```

```python
def vs.SetRRDiam(h, xDiam, yDiam):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|xDiam|REAL|   |
|yDiam|REAL|   |

## Examples
```pascal
SetRRDiam(h, 1.0, 2.0);
```
```python
import vs

# Sets the diameters of a rounded rectangle.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
xDiam = 1.0
yDiam = 2.0

vs.SetRRDiam(h, xDiam, yDiam)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Object Editing](../Categories/Object%20Editing.md)
