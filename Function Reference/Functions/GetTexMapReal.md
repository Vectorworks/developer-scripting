# GetTexMapReal

## Description
Get map info for specific part of object. partID is texture part, overall is 3.

Selector:
*offsetX:1
*offsetY:2
*scale2D:3
*rotate2D:4
*radius:5
*matrix mat00 through mat32: 6-17
:These values are the coefficients for the 4 row x 3 column object space to texture space 3D transform matrix.  These values are changed by things like the Edit Mapping dialog.

```pascal
FUNCTION GetTexMapReal(
				h        : HANDLE;
				partID   : LONGINT;
				selector : INTEGER): REAL;
```

```python
def vs.GetTexMapReal(h, partID, selector):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|partID|LONGINT|texture part, overall is 3.|
|selector|INTEGER|offsetX:1, offsetY:2, scale2D:3, rotate2D:4, radius:5, matrix mat00 through mat32: 6-17|

## See Also
* [SetTexMapReal](SetTexMapReal.md) VW 14
* [SetTexMapRealN](SetTexMapRealN.md) from VW 15
* [GetTexMapRealN](GetTexMapRealN.md) from VW 15

## Version
Availability: from Vectorworks 14.0. Deprecated from Vectorworks 15.

## Category
* [Textures](../Categories/Textures.md)
