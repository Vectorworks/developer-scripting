# SetTexMapInt

## Description
Set map info for specific part of object. partID is texture part, overall is 3. Selector should be 1 to set the map type integer.

```pascal
PROCEDURE SetTexMapInt(
				h        : HANDLE;
				partID   : LONGINT;
				selector : INTEGER;
				value    : INTEGER);
```

```python
def vs.SetTexMapInt(h, partID, selector, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|partID|LONGINT|   |
|selector|INTEGER|   |
|value|INTEGER|   |

## Remarks
Value is one of the:
```pascal
kPlaneSpace = 0;
kSphereSpace = 1;
kCylinderSpace = 2;
kAlgorithmicSpace = 3; {Space that wraps around the object most}
```

Algorithmic means either the "perimeter" or "roof" mapping type.

## Examples
```pascal
BEGIN
	SetTexMapInt (LNewObj,3,1,0);
	SetTexMapReal (LNewObj,3,4, Deg2Rad(0));
END ELSE
BEGIN
	SetTexMapInt (LNewObj,3,1,0);

SetTexMapBool (DummyWholeHandle,kTexturePartID,1,TRUE);
SetTexMapInt (DummyWholeHandle,kTexturePartID,1,3);

BEGIN
	SetDefaultTexMap (hGoods);
	IF ImageTextIndex <> 0 THEN settexturerefN(hGoods,ImageTextIndex,kTexturePartID,kTextureLayerID);
	SetTexMapBool (hGoods,kTexturePartID,1,TRUE);
	SetTexMapInt (hGoods,kTexturePartID,1,3);
```
```python
import vs

# Set map info for specific part of object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
partID = 1
selector = 2
value = 3

vs.SetTexMapInt(h, partID, selector, value)
```

## See Also
[GetTexMapInt](GetTexMapInt.md)

## Version
Availability: from Vectorworks14.0

## Category
* [Textures](../Categories/Textures.md)
