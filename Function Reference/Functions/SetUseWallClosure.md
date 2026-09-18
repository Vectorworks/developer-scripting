# SetUseWallClosure

## Description
Sets the use wall closure setting of a symbol definition, plug-in object style, or plug-in object.

```pascal
FUNCTION SetUseWallClosure(
				hObject        : HANDLE;
				useWallClosure : BOOLEAN): BOOLEAN;
```

```python
def vs.SetUseWallClosure(hObject, useWallClosure):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|
|useWallClosure|BOOLEAN|The use wall closure setting.|

## Examples
```pascal
resultOK := SetUseWallClosure(hObject, TRUE);
```
```python
import vs

# Sets the use wall closure setting of a symbol definition, plug-in object
# style, or plug-in object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
useWallClosure = True

ok = vs.SetUseWallClosure(hObject, useWallClosure)
if ok:
    vs.Message('SetUseWallClosure succeeded')
else:
    vs.Message('SetUseWallClosure failed')
```

## See Also
VS Functions:
[GetUseWallClosure](GetUseWallClosure.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
