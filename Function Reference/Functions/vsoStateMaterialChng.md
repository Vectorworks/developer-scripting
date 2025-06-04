# vsoStateMaterialChng

## Description
ObjectState event is sent to Parametric objects when Material is changed.

```pascal
FUNCTION vsoStateMaterialChng(
				hObj                : HANDLE;
				VAR materialID      : INTEGER;
				VAR deleted         : BOOLEAN;
				VAR previousTexture : INTEGER): BOOLEAN;
```

```python
def vs.vsoStateMaterialChng(hObj):
    return (BOOLEAN, materialID, deleted, previousTexture)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE|   |
|materialID|INTEGER|   |
|deleted|BOOLEAN|   |
|previousTexture|INTEGER|   |

## Version
Availability: from Vectorworks 2020

## Category
* [Object Events](../Categories/Object%20Events.md)
