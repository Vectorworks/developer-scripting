# SetVertSecCPByStyle

```pascal
FUNCTION SetVertSecCPByStyle(
				hObject : HANDLE;
				byStyle : BOOLEAN): BOOLEAN;
```

```python
def vs.SetVertSecCPByStyle(hObject, byStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|byStyle|BOOLEAN|   |

## Examples
```pascal
resultOK := SetVertSecCPByStyle(hObject, TRUE);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
byStyle = True

ok = vs.SetVertSecCPByStyle(hObject, byStyle)
if ok:
    vs.Message('SetVertSecCPByStyle succeeded')
else:
    vs.Message('SetVertSecCPByStyle failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
