# SetUseWllClsrByStyle

## Description
Sets whether the use wall closure setting of a symbol definition, plug-in object style, or plug-in object is by style.

```pascal
FUNCTION SetUseWllClsrByStyle(
				hObject : HANDLE;
				byStyle : BOOLEAN): BOOLEAN;
```

```python
def vs.SetUseWllClsrByStyle(hObject, byStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|
|byStyle|BOOLEAN|Whether the use wall closure setting is by style.|

## Examples
```pascal
resultOK := SetUseWllClsrByStyle(hObject, TRUE);
```
```python
import vs

# Sets whether the use wall closure setting of a symbol definition, plug-in
# object style, or plug-in object is by style.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
byStyle = True

ok = vs.SetUseWllClsrByStyle(hObject, byStyle)
if ok:
    vs.Message('SetUseWllClsrByStyle succeeded')
else:
    vs.Message('SetUseWllClsrByStyle failed')
```

## See Also
VS Functions:
[GetUseWllClsrByStyle](GetUseWllClsrByStyle.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
