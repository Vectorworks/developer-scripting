# GetTpPl2DCompByStyle

```pascal
FUNCTION GetTpPl2DCompByStyle(hObject : HANDLE): BOOLEAN;
```

```python
def vs.GetTpPl2DCompByStyle(hObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |

## Examples
```pascal
resultOK := GetTpPl2DCompByStyle(hObject);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetTpPl2DCompByStyle(hObject)
if ok:
    vs.Message('GetTpPl2DCompByStyle succeeded')
else:
    vs.Message('GetTpPl2DCompByStyle failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
