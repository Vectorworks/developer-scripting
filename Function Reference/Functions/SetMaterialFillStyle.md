# SetMaterialFillStyle

```pascal
FUNCTION SetMaterialFillStyle(
				materialHandle : HANDLE;
				fillStyle      : LONGINT): BOOLEAN;
```

```python
def vs.SetMaterialFillStyle(materialHandle, fillStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|materialHandle|HANDLE|   |
|fillStyle|LONGINT|InternalIndex of fillStyle|

## Examples
```pascal
resultOK := SetMaterialFillStyle(materialHandle, 1);
```
```python
import vs

materialHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
fillStyle = 0

ok = vs.SetMaterialFillStyle(materialHandle, fillStyle)
if ok:
    vs.Message('SetMaterialFillStyle succeeded')
else:
    vs.Message('SetMaterialFillStyle failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
