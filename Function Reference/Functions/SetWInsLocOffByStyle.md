# SetWInsLocOffByStyle

## Description
Sets whether the wall insert location offset of a symbol definition, plug-in object style, or plug-in object is by style.

```pascal
FUNCTION SetWInsLocOffByStyle(
				hObject : HANDLE;
				byStyle : BOOLEAN): BOOLEAN;
```

```python
def vs.SetWInsLocOffByStyle(hObject, byStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|
|byStyle|BOOLEAN|Whether the wall insert location offset is by style.|

## Examples
```pascal
resultOK := SetWInsLocOffByStyle(hObject, TRUE);
```
```python
import vs

# Sets whether the wall insert location offset of a symbol definition,
# plug-in object style, or plug-in object is by style.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
byStyle = True

ok = vs.SetWInsLocOffByStyle(hObject, byStyle)
if ok:
    vs.Message('SetWInsLocOffByStyle succeeded')
else:
    vs.Message('SetWInsLocOffByStyle failed')
```

## See Also
VS Functions:
[GetWInsLocOffByStyle](GetWInsLocOffByStyle.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
