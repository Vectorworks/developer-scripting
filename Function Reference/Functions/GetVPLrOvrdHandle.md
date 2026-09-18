# GetVPLrOvrdHandle

## Description
Retrieves the handle of the layer overridden at the specified index in the overrides list.

```pascal
FUNCTION GetVPLrOvrdHandle(
				viewportHandle : HANDLE;
				index          : INTEGER): HANDLE;
```

```python
def vs.GetVPLrOvrdHandle(viewportHandle, index):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|index|INTEGER|The index into the layer overrides list.|

## Examples
```pascal
resultH := GetVPLrOvrdHandle(viewportHandle, 1);
```
```python
import vs

# Retrieves the handle of the layer overridden at the specified index in the
# overrides list.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1

objHandle = vs.GetVPLrOvrdHandle(viewportHandle, index)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[GetVPLrOvrdCount](GetVPLrOvrdCount.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
