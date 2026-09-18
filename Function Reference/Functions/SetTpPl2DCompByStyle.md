# SetTpPl2DCompByStyle

```pascal
FUNCTION SetTpPl2DCompByStyle(
				hObject : HANDLE;
				byStyle : BOOLEAN): BOOLEAN;
```

```python
def vs.SetTpPl2DCompByStyle(hObject, byStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|byStyle|BOOLEAN|   |

## Examples
```pascal
resultOK := SetTpPl2DCompByStyle(hObject, TRUE);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
byStyle = True

ok = vs.SetTpPl2DCompByStyle(hObject, byStyle)
if ok:
    vs.Message('SetTpPl2DCompByStyle succeeded')
else:
    vs.Message('SetTpPl2DCompByStyle failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
