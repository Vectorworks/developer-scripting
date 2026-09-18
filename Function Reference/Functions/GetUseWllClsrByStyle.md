# GetUseWllClsrByStyle

## Description
Gets whether the use wall closure setting of a symbol definition, plug-in object style, or plug-in object is by style.

```pascal
FUNCTION GetUseWllClsrByStyle(hObject : HANDLE): BOOLEAN;
```

```python
def vs.GetUseWllClsrByStyle(hObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|

## Examples
```pascal
resultOK := GetUseWllClsrByStyle(hObject);
```
```python
import vs

# Gets whether the use wall closure setting of a symbol definition, plug-in
# object style, or plug-in object is by style.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetUseWllClsrByStyle(hObject)
if ok:
    vs.Message('GetUseWllClsrByStyle succeeded')
else:
    vs.Message('GetUseWllClsrByStyle failed')
```

## See Also
VS Functions:
[SetUseWllClsrByStyle](SetUseWllClsrByStyle.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
