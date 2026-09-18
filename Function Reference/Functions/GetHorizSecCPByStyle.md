# GetHorizSecCPByStyle

```pascal
FUNCTION GetHorizSecCPByStyle(hObject : HANDLE): BOOLEAN;
```

```python
def vs.GetHorizSecCPByStyle(hObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |

## Examples
```pascal
resultOK := GetHorizSecCPByStyle(hObject);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.GetHorizSecCPByStyle(hObject)
if ok:
    vs.Message('GetHorizSecCPByStyle succeeded')
else:
    vs.Message('GetHorizSecCPByStyle failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
