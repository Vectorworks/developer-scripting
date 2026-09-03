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

## Examples
```pascal
BEGIN
	{AlrtDialog('About to call  vsoStateMaterialChng at Column!!');}
	resultStatus := vsoStateMaterialChng(gPluginH, updatedMaterialID, materialDeleted, prevTexture);
```
```python
import vs

# ObjectState event is sent to Parametric objects when Material is changed.
hObj = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, materialID, deleted, previousTexture = vs.vsoStateMaterialChng(hObj)
vs.Message('vsoStateMaterialChng returned: ' + str((ok, materialID, deleted, previousTexture)))
```

## Version
Availability: from Vectorworks 2020

## Category
* [Object Events](../Categories/Object%20Events.md)
