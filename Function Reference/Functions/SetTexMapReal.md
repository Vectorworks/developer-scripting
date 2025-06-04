# SetTexMapReal

## Description
Set map info for specific part of object. partID is texture part, overall is 3.

Selector:
*offsetX:1
*offsetY:2
*scale2D:3
*rotate2D:4
*radius:5
*matrix mat00 through mat32: 6-17
:These values are the coefficients for the 4 row x 3 column object space to texture space 3D transform matrix.  These values are changed by things like the Edit Mapping dialog.

```pascal
PROCEDURE SetTexMapReal(
				h        : HANDLE;
				partID   : LONGINT;
				selector : INTEGER;
				value    : REAL);
```

```python
def vs.SetTexMapReal(h, partID, selector, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|partID|LONGINT|   |
|selector|INTEGER|   |
|value|REAL|   |

## See Also
[GetTexMapReal](GetTexMapReal.md)

## Version
Availability: from Vectorworks14.0

## Category
* [Textures](../Categories/Textures.md)
