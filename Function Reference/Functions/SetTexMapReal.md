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

## Examples
```pascal
BEGIN
    SetDefaultTexMap (slab_h);
	if openDoor then
		SetTexMapReal (slab_h,3,4, angOpened )
	else
		SetTexMapReal (slab_h,3,4, angClosed);

SetTexMapReal (DummyWholeHandle,kTexturePartID,3,Scaleim*DummyLength/GetObjectVariableREAL(TexObjHan,511));

BEGIN
	SetTexMapBool (hGoods,kTexturePartID,2,(TRUE));
	IF NOT (GetBool('Flat3D')) THEN
			SetTexMapReal (hGoods,kTexturePartID,4,Deg2Rad(-90))
					ELSE
				SetTexMapReal (hGoods,kTexturePartID,4,Deg2Rad(-90));
END
```
```python
import vs

# Set map info for specific part of object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
partID = 1
selector = 2
value = 1.0

vs.SetTexMapReal(h, partID, selector, value)
```

## See Also
[GetTexMapReal](GetTexMapReal.md)

## Version
Availability: from Vectorworks14.0

## Category
* [Textures](../Categories/Textures.md)
