# GetWallInsLocByStyle

## Description
Gets whether the wall insert location of a symbol definition, plug-in object style, or plug-in object is by style.

```pascal
FUNCTION GetWallInsLocByStyle(hObject : HANDLE): BOOLEAN;
```

```python
def vs.GetWallInsLocByStyle(hObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|

## Examples
```pascal
resultOK := GetWallInsLocByStyle(hObject);
```
```python
import vs

# Gets whether the wall insert location of a symbol definition, plug-in
# object style, or plug-in object is by style.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetWallInsLocByStyle(hObject)
if ok:
    vs.Message('GetWallInsLocByStyle succeeded')
else:
    vs.Message('GetWallInsLocByStyle failed')
```

## See Also
VS Functions:
[SetWallInsLocByStyle](SetWallInsLocByStyle.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
