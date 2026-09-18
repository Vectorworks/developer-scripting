# GetUseWallClosure

## Description
Gets the use wall closure setting of a symbol definition, plug-in object style, or plug-in object.

```pascal
FUNCTION GetUseWallClosure(hObject : HANDLE): BOOLEAN;
```

```python
def vs.GetUseWallClosure(hObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|

## Examples
```pascal
resultOK := GetUseWallClosure(hObject);
```
```python
import vs

# Gets the use wall closure setting of a symbol definition, plug-in object
# style, or plug-in object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetUseWallClosure(hObject)
if ok:
    vs.Message('GetUseWallClosure succeeded')
else:
    vs.Message('GetUseWallClosure failed')
```

## See Also
VS Functions:
[SetUseWallClosure](SetUseWallClosure.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
