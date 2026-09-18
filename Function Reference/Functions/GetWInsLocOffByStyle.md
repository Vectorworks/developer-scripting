# GetWInsLocOffByStyle

## Description
Gets whether the wall insert location offset of a symbol definition, plug-in object style, or plug-in object is by style.

```pascal
FUNCTION GetWInsLocOffByStyle(hObject : HANDLE): BOOLEAN;
```

```python
def vs.GetWInsLocOffByStyle(hObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|

## Examples
```pascal
resultOK := GetWInsLocOffByStyle(hObject);
```
```python
import vs

# Gets whether the wall insert location offset of a symbol definition,
# plug-in object style, or plug-in object is by style.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetWInsLocOffByStyle(hObject)
if ok:
    vs.Message('GetWInsLocOffByStyle succeeded')
else:
    vs.Message('GetWInsLocOffByStyle failed')
```

## See Also
VS Functions:
[SetWInsLocOffByStyle](SetWInsLocOffByStyle.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
