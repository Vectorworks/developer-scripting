# SetTexMapBool

## Description
Set map info for specific part of object. partID is texture part, overall is 3.

Selector:
*init:1
*flip:2
*repH:3
*repV:4
*long edge:5
*worldZ:6
*auto align:7

```pascal
PROCEDURE SetTexMapBool(
				h        : HANDLE;
				partID   : LONGINT;
				selector : INTEGER;
				value    : BOOLEAN);
```

```python
def vs.SetTexMapBool(h, partID, selector, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|partID|LONGINT|   |
|selector|INTEGER|   |
|value|BOOLEAN|   |

## Remarks
The init value is whether the texture mapping info contains valid information.  If the mapping is not really set to important values then the init value will be false.  This can happen if the mapping was not set with [SetDefaultTexMap](SetDefaultTexMap.md).

## Examples
```pascal
SetTexMapBool (DummyWholeHandle,kTexturePartID,1,TRUE);
SetTexMapInt (DummyWholeHandle,kTexturePartID,1,3);

BEGIN
	SetTexMapBool (hGoods,kTexturePartID,2,(TRUE));
	IF NOT (GetBool('Flat3D')) THEN
			SetTexMapReal (hGoods,kTexturePartID,4,Deg2Rad(-90))
					ELSE
				SetTexMapReal (hGoods,kTexturePartID,4,Deg2Rad(-90));
```
```python
import vs

# Set map info for specific part of object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
partID = 1
selector = 2
value = True

vs.SetTexMapBool(h, partID, selector, value)
```

## See Also
[GetTexMapBool](GetTexMapBool.md) | [SetDefaultTexMap](SetDefaultTexMap.md)

## Version
Availability: from Vectorworks14.0

## Category
* [Textures](../Categories/Textures.md)
