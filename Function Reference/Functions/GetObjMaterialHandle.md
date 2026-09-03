# GetObjMaterialHandle

```pascal
FUNCTION GetObjMaterialHandle(h : HANDLE): HANDLE;
```

```python
def vs.GetObjMaterialHandle(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|object handle|

## Examples
```pascal
resultH := GetObjMaterialHandle(h);
```
```python
import vs

h = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetObjMaterialHandle(h)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
