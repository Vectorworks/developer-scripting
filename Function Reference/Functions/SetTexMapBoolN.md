# SetTexMapBoolN

## Description
Set map info for specific part of object. partID is texture part, overall is 3. Selector: init:1, flip:2, repH:3, repV:4, long edge:5, worldZ:6, auto align:7

```pascal
PROCEDURE SetTexMapBoolN(
				obj        : HANDLE;
				texPartID  : LONGINT;
				texLayerID : LONGINT;
				selector   : INTEGER;
				value      : BOOLEAN);
```

```python
def vs.SetTexMapBoolN(obj, texPartID, texLayerID, selector, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|   |
|texPartID|LONGINT|   |
|texLayerID|LONGINT|   |
|selector|INTEGER|   |
|value|BOOLEAN|   |

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
