# HScale3D

## Description
Scales a 3D object.

```pascal
PROCEDURE HScale3D(
				h       : HANDLE;
				centerX : REAL;
				centerY : REAL;
				centerZ : REAL;
				scaleX  : REAL;
				scaleY  : REAL;
				scaleZ  : REAL);
```

```python
def vs.HScale3D(h, centerX, centerY, centerZ, scaleX, scaleY, scaleZ):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|centerX|REAL|   |
|centerY|REAL|   |
|centerZ|REAL|   |
|scaleX|REAL|   |
|scaleY|REAL|   |
|scaleZ|REAL|   |

## Remarks
[Ptr 07/17/2019] Unlike for the HScale2D command, scaleX, scaleY and scaleZ can NOT be negative. If so, the function does nothing.

[Ptr 02/02/2024] This command doesn't work on symbols.

## Examples
```pascal
HScale3D( objH1, 0, 0, 0, a, b, c );
```
```python
import vs

# Scales a 3D object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
centerX = 1.0
centerY = 2.0
centerZ = 0.5
scaleX = 1.0
scaleY = 1.0
scaleZ = 1.0

vs.HScale3D(h, centerX, centerY, centerZ, scaleX, scaleY, scaleZ)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Object Editing](../Categories/Object%20Editing.md)
