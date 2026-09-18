# Get2DCompByStyle

```pascal
FUNCTION Get2DCompByStyle(hObject : HANDLE): BOOLEAN;
```

```python
def vs.Get2DCompByStyle(hObject):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |

## Examples
```pascal
resultOK := Get2DCompByStyle(hObject);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.Get2DCompByStyle(hObject)
if ok:
    vs.Message('Get2DCompByStyle succeeded')
else:
    vs.Message('Get2DCompByStyle failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
