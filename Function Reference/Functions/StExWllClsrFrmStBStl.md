# StExWllClsrFrmStBStl

## Description
Sets whether the exclude wall closure from settings of a symbol definition, plug-in object style, or plug-in object are by style.

```pascal
FUNCTION StExWllClsrFrmStBStl(
				hObject : HANDLE;
				byStyle : BOOLEAN): BOOLEAN;
```

```python
def vs.StExWllClsrFrmStBStl(hObject, byStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|
|byStyle|BOOLEAN|Whether the exclude wall closure from settings of a symbol definition, plug-in object style, or plug-in object are by style.|

## Examples
```pascal
resultOK := StExWllClsrFrmStBStl(hObject, TRUE);
```
```python
import vs

# Sets whether the exclude wall closure from settings of a symbol definition,
# plug-in object style, or plug-in object are by style.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
byStyle = True

ok = vs.StExWllClsrFrmStBStl(hObject, byStyle)
if ok:
    vs.Message('StExWllClsrFrmStBStl succeeded')
else:
    vs.Message('StExWllClsrFrmStBStl failed')
```

## See Also
VS Functions:
[GtExWllClsrFrmStBStl](GtExWllClsrFrmStBStl.md)

## Version
Availability: from Vectorworks 2023

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
