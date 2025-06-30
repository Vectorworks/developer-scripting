# SetTexMapRealN

## Description
Set map info for specific part of object. partID is texture part, overall is 3. Selector: offsetX:1, offsetY:2, scale2D:3, rotate2D:4, radius:5, matrix mat00 through mat32: 6-17

```pascal
PROCEDURE SetTexMapRealN(
				obj        : HANDLE;
				texPartID  : LONGINT;
				texLayerID : LONGINT;
				selector   : INTEGER;
				value      : REAL);
```

```python
def vs.SetTexMapRealN(obj, texPartID, texLayerID, selector, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |
|texPartID|LONGINT|   |
|texLayerID|LONGINT|0 for base, >0 for decals|
|selector|INTEGER|   |
|value|REAL|   |

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
