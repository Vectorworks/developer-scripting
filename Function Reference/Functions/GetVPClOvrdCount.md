# GetVPClOvrdCount

## Description
Returns the number of class overrides associated with a particular viewport.

```pascal
FUNCTION GetVPClOvrdCount(viewportHandle : HANDLE): INTEGER;
```

```python
def vs.GetVPClOvrdCount(viewportHandle):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|

## Examples
```pascal
resultN := GetVPClOvrdCount(viewportHandle);
```
```python
import vs

# Returns the number of class overrides associated with a particular viewport.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.GetVPClOvrdCount(viewportHandle)
vs.Message('GetVPClOvrdCount returned: ' + str(count))
```

## See Also
VS Functions:
[GetVPClOvrdName](GetVPClOvrdName.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
