# GetVPLrOvrdCount

## Description
Retrieves the number of layer overrides.

```pascal
FUNCTION GetVPLrOvrdCount(viewportHandle : HANDLE): INTEGER;
```

```python
def vs.GetVPLrOvrdCount(viewportHandle):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|

## Examples
```pascal
resultN := GetVPLrOvrdCount(viewportHandle);
```
```python
import vs

# Retrieves the number of layer overrides.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.GetVPLrOvrdCount(viewportHandle)
vs.Message('GetVPLrOvrdCount returned: ' + str(count))
```

## See Also
VS Functions:
[GetVPLrOvrdHandle](GetVPLrOvrdHandle.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
