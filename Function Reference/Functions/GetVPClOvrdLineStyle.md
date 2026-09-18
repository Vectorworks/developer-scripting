# GetVPClOvrdLineStyle

```pascal
FUNCTION GetVPClOvrdLineStyle(
				viewportHandle : HANDLE;
				className      : STRING): LONGINT;
```

```python
def vs.GetVPClOvrdLineStyle(viewportHandle, className):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|className|STRING|The name of the class override.|

## Examples
```pascal
resultN := GetVPClOvrdLineStyle(viewportHandle, 'Wall');
```
```python
import vs

viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'

resultN = vs.GetVPClOvrdLineStyle(viewportHandle, className)
vs.Message('GetVPClOvrdLineStyle returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Viewports](../Categories/Viewports.md)
