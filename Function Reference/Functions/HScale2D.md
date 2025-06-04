# HScale2D

## Description
Scales a 2D object.

```pascal
PROCEDURE HScale2D(
				h         : HANDLE;
				centerX   : REAL;
				centerY   : REAL;
				scaleX    : REAL;
				scaleY    : REAL;
				scaleText : BOOLEAN);
```

```python
def vs.HScale2D(h, centerX, centerY, scaleX, scaleY, scaleText):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|centerX|REAL|   |
|centerY|REAL|   |
|scaleX|REAL|   |
|scaleY|REAL|   |
|scaleText|BOOLEAN|   |

## Remarks
If (scaleX = -1) or (scaleY = -1) the object will be mirrored.

If used on an extrude, the 2D shape inside the extrude will be scaled. The scaling will follow the 2D shape's working plane.

[Ptr 07/17/2019]

## Version
Availability: from Vectorworks 2014

## Category
* [Object Editing](../Categories/Object%20Editing.md)
