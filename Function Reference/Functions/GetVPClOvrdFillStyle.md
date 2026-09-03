# GetVPClOvrdFillStyle

```pascal
FUNCTION GetVPClOvrdFillStyle(
				viewportHandle : HANDLE;
				className      : STRING): LONGINT;
```

```python
def vs.GetVPClOvrdFillStyle(viewportHandle, className):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport Handle|
|className|STRING|The name of the class override|

## Examples
```pascal
resultN := GetVPClOvrdFillStyle(viewportHandle, 'Wall');
```
```python
import vs

viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'

resultN = vs.GetVPClOvrdFillStyle(viewportHandle, className)
vs.Message('GetVPClOvrdFillStyle returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Viewports](../Categories/Viewports.md)
