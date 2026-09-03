# GetVPClOvrdFillOpty

## Description
Retrieves the fill opacity for a viewport class override.

```pascal
FUNCTION GetVPClOvrdFillOpty(
				viewportHandle : HANDLE;
				className      : STRING): INTEGER;
```

```python
def vs.GetVPClOvrdFillOpty(viewportHandle, className):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|className|STRING|Name of the class.|

## Examples
```pascal
resultN := GetVPClOvrdFillOpty(viewportHandle, 'Wall');
```
```python
import vs

# Retrieves the fill opacity for a viewport class override.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'

resultN = vs.GetVPClOvrdFillOpty(viewportHandle, className)
vs.Message('GetVPClOvrdFillOpty returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetVPClOvrdFillOpty](SetVPClOvrdFillOpty.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
