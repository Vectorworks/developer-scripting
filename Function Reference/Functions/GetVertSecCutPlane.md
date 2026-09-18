# GetVertSecCutPlane

```pascal
FUNCTION GetVertSecCutPlane(hObject : HANDLE): INTEGER;
```

```python
def vs.GetVertSecCutPlane(hObject):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |

## Remarks
*\_c\_* (2021.01.31): Constants returned:
* 1 = View as Cut when Cut in Viewport
* 3 = View as Uncut beyond when Cut in Viewport
* 4 = View as Uncut before when Cut in Viewport

## Examples
```pascal
resultN := GetVertSecCutPlane(hObject);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetVertSecCutPlane(hObject)
vs.Message('GetVertSecCutPlane returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
