# RemoveVPLrOvrd

## Description
Removes a layer override.

```pascal
PROCEDURE RemoveVPLrOvrd(
				viewportHandle : HANDLE;
				layerHandle    : HANDLE);
```

```python
def vs.RemoveVPLrOvrd(viewportHandle, layerHandle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|layerHandle|HANDLE|The layer handle.|

## Examples
```pascal
RemoveVPLrOvrd(viewportHandle, layerHandle);
```
```python
import vs

# Removes a layer override.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
layerHandle = vs.ActLayer()  # handle to the active design layer

vs.RemoveVPLrOvrd(viewportHandle, layerHandle)
```

## See Also
VS Functions:
[CreateVPLrOvrd](CreateVPLrOvrd.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
