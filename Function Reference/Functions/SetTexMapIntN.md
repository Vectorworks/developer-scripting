# SetTexMapIntN

## Description
Set map info for specific part of object. partID is texture part, overall is 3. Selector should be 1 to set the map type integer.

```pascal
PROCEDURE SetTexMapIntN(
				obj        : HANDLE;
				texPartID  : LONGINT;
				texLayerID : LONGINT;
				selector   : INTEGER;
				value      : INTEGER);
```

```python
def vs.SetTexMapIntN(obj, texPartID, texLayerID, selector, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |
|texPartID|LONGINT|   |
|texLayerID|LONGINT|0 for base, >0 for decals|
|selector|INTEGER|   |
|value|INTEGER|   |

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
