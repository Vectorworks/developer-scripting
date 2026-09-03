# GetClassByStyle

```pascal
FUNCTION GetClassByStyle(hObject : HANDLE): BOOLEAN;
```

```python
def vs.GetClassByStyle(hObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |

## Examples
```pascal
resultOK := GetClassByStyle(hObject);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetClassByStyle(hObject)
if ok:
    vs.Message('GetClassByStyle succeeded')
else:
    vs.Message('GetClassByStyle failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
