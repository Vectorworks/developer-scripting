# SetHorizSecCPByStyle

```pascal
FUNCTION SetHorizSecCPByStyle(
				hObject : HANDLE;
				byStyle : BOOLEAN): BOOLEAN;
```

```python
def vs.SetHorizSecCPByStyle(hObject, byStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|byStyle|BOOLEAN|   |

## Examples
```pascal
resultOK := SetHorizSecCPByStyle(hObject, TRUE);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
byStyle = True

ok = vs.SetHorizSecCPByStyle(hObject, byStyle)
if ok:
    vs.Message('SetHorizSecCPByStyle succeeded')
else:
    vs.Message('SetHorizSecCPByStyle failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
