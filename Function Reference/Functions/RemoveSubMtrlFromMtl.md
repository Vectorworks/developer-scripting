# RemoveSubMtrlFromMtl

## Description
Removes a Simple material from a Compound material.

```pascal
FUNCTION RemoveSubMtrlFromMtl(
				hMaterial   : HANDLE;
				subMtrlName : STRING): Boolean;
```

```python
def vs.RemoveSubMtrlFromMtl(hMaterial, subMtrlName):
    return Boolean
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hMaterial|HANDLE|Handle of a Compound material|
|subMtrlName|STRING|Name of a Simple material to be deleted|

## Examples
```pascal
resultOK := RemoveSubMtrlFromMtl(hMaterial, 'Example');
```
```python
import vs

# Removes a Simple material from a Compound material.
hMaterial = vs.FSActLayer()  # handle to the first selected object on the active layer
subMtrlName = 'Example'

ok = vs.RemoveSubMtrlFromMtl(hMaterial, subMtrlName)
if ok:
    vs.Message('RemoveSubMtrlFromMtl succeeded')
else:
    vs.Message('RemoveSubMtrlFromMtl failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
