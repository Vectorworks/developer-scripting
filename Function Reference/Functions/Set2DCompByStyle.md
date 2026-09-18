# Set2DCompByStyle

```pascal
FUNCTION Set2DCompByStyle(
				hObject : HANDLE;
				byStyle : BOOLEAN): BOOLEAN;
```

```python
def vs.Set2DCompByStyle(hObject, byStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|byStyle|BOOLEAN|   |

## Examples
```pascal
resultOK := Set2DCompByStyle(hObject, TRUE);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
byStyle = True

ok = vs.Set2DCompByStyle(hObject, byStyle)
if ok:
    vs.Message('Set2DCompByStyle succeeded')
else:
    vs.Message('Set2DCompByStyle failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
