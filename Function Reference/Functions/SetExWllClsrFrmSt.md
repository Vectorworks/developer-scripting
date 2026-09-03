# SetExWllClsrFrmSt

## Description
Sets the exclude wall closure from settings of a symbol definition, plug-in object style, or plug-in object.

```pascal
FUNCTION SetExWllClsrFrmSt(
				hObject : HANDLE;
				left    : BOOLEAN;
				right   : BOOLEAN;
				top     : BOOLEAN;
				bottom  : BOOLEAN): BOOLEAN;
```

```python
def vs.SetExWllClsrFrmSt(hObject, left, right, top, bottom):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|
|left|BOOLEAN|The exclude wall closure from left setting.|
|right|BOOLEAN|The exclude wall closure from right setting.|
|top|BOOLEAN|The exclude wall closure from top setting.|
|bottom|BOOLEAN|The exclude wall closure from bottom setting.|

## Examples
```pascal
resultOK := SetExWllClsrFrmSt(hObject, TRUE, FALSE, TRUE, TRUE);
```
```python
import vs

# Sets the exclude wall closure from settings of a symbol definition, plug-in
# object style, or plug-in object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
left = True
right = True
top = True
bottom = True

ok = vs.SetExWllClsrFrmSt(hObject, left, right, top, bottom)
if ok:
    vs.Message('SetExWllClsrFrmSt succeeded')
else:
    vs.Message('SetExWllClsrFrmSt failed')
```

## See Also
VS Functions:
[GetExWllClsrFrmSt](GetExWllClsrFrmSt.md)

## Version
Availability: from Vectorworks 2023

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
