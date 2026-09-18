# GetVPClOvrdObjTxt

```pascal
FUNCTION GetVPClOvrdObjTxt(
				viewportHandle : HANDLE;
				className      : STRING): INTEGER;
```

```python
def vs.GetVPClOvrdObjTxt(viewportHandle, className):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle|
|className|STRING|The name of the class override|

## Examples
```pascal
resultN := GetVPClOvrdObjTxt(viewportHandle, 'Wall');
```
```python
import vs

viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'

resultN = vs.GetVPClOvrdObjTxt(viewportHandle, className)
vs.Message('GetVPClOvrdObjTxt returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Viewports](../Categories/Viewports.md)
