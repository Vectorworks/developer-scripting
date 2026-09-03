# GetVertSecCPByStyle

```pascal
FUNCTION GetVertSecCPByStyle(hObject : HANDLE): BOOLEAN;
```

```python
def vs.GetVertSecCPByStyle(hObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |

## Examples
```pascal
resultOK := GetVertSecCPByStyle(hObject);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetVertSecCPByStyle(hObject)
if ok:
    vs.Message('GetVertSecCPByStyle succeeded')
else:
    vs.Message('GetVertSecCPByStyle failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
