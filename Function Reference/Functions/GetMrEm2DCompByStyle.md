# GetMrEm2DCompByStyle

```pascal
FUNCTION GetMrEm2DCompByStyle(hObject : HANDLE): BOOLEAN;
```

```python
def vs.GetMrEm2DCompByStyle(hObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |

## Examples
```pascal
resultOK := GetMrEm2DCompByStyle(hObject);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetMrEm2DCompByStyle(hObject)
if ok:
    vs.Message('GetMrEm2DCompByStyle succeeded')
else:
    vs.Message('GetMrEm2DCompByStyle failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
