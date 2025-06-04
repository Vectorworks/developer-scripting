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

## Version
Availability: from Vectorworks 2014

## Category
* [Object Editing](../Categories/Object%20Editing.md)
