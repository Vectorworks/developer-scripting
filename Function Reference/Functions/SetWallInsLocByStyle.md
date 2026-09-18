# SetWallInsLocByStyle

## Description
Sets whether the wall insert location of a symbol definition, plug-in object style, or plug-in object is by style.

```pascal
FUNCTION SetWallInsLocByStyle(
				hObject : HANDLE;
				byStyle : BOOLEAN): BOOLEAN;
```

```python
def vs.SetWallInsLocByStyle(hObject, byStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|
|byStyle|BOOLEAN|Whether the wall insert location is by style.|

## Examples
```pascal
resultOK := SetWallInsLocByStyle(hObject, TRUE);
```
```python
import vs

# Sets whether the wall insert location of a symbol definition, plug-in
# object style, or plug-in object is by style.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
byStyle = True

ok = vs.SetWallInsLocByStyle(hObject, byStyle)
if ok:
    vs.Message('SetWallInsLocByStyle succeeded')
else:
    vs.Message('SetWallInsLocByStyle failed')
```

## See Also
VS Functions:
[GetWallInsLocByStyle](GetWallInsLocByStyle.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
