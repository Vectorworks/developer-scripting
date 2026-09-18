# SetClassByStyle

```pascal
FUNCTION SetClassByStyle(
				hObject : HANDLE;
				byStyle : BOOLEAN): BOOLEAN;
```

```python
def vs.SetClassByStyle(hObject, byStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|byStyle|BOOLEAN|   |

## Examples
```pascal
resultOK := SetClassByStyle(hObject, TRUE);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
byStyle = True

ok = vs.SetClassByStyle(hObject, byStyle)
if ok:
    vs.Message('SetClassByStyle succeeded')
else:
    vs.Message('SetClassByStyle failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
