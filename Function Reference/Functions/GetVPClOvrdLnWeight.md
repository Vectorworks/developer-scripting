# GetVPClOvrdLnWeight

```pascal
FUNCTION GetVPClOvrdLnWeight(
				viewportHandle : HANDLE;
				className      : STRING): INTEGER;
```

```python
def vs.GetVPClOvrdLnWeight(viewportHandle, className):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The handle of the viewport|
|className|STRING|The name of the class override|

## Examples
```pascal
resultN := GetVPClOvrdLnWeight(viewportHandle, 'Wall');
```
```python
import vs

viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'

resultN = vs.GetVPClOvrdLnWeight(viewportHandle, className)
vs.Message('GetVPClOvrdLnWeight returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Viewports](../Categories/Viewports.md)
