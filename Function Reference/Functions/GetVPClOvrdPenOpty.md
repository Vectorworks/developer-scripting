# GetVPClOvrdPenOpty

## Description
Retrieves the pen opacity for a class override. Opacity is in the range 0-100.

```pascal
FUNCTION GetVPClOvrdPenOpty(
				viewportHandle : HANDLE;
				className      : STRING): INTEGER;
```

```python
def vs.GetVPClOvrdPenOpty(viewportHandle, className):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|className|STRING|Name of the class.|

## Examples
```pascal
resultN := GetVPClOvrdPenOpty(viewportHandle, 'Wall');
```
```python
import vs

# Retrieves the pen opacity for a class override.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'

resultN = vs.GetVPClOvrdPenOpty(viewportHandle, className)
vs.Message('GetVPClOvrdPenOpty returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetVPClOvrdPenOpty](SetVPClOvrdPenOpty.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
