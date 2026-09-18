# GetHorizSecCutPlane

```pascal
FUNCTION GetHorizSecCutPlane(hObject : HANDLE): INTEGER;
```

```python
def vs.GetHorizSecCutPlane(hObject):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |

## Remarks
*\_c\_* (2021.01.31): Constants returned:
* 1 = View as Cut when Cut in Viewport
* 3 = View as Uncut below when Cut in Viewport
* 4 = View as Uncut above when Cut in Viewport

## Examples
```pascal
resultN := GetHorizSecCutPlane(hObject);
```
```python
import vs

hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetHorizSecCutPlane(hObject)
vs.Message('GetHorizSecCutPlane returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2020

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
