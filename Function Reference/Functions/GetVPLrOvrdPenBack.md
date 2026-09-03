# GetVPLrOvrdPenBack

## Description
Gets the pen background color from a layer override.

```pascal
PROCEDURE GetVPLrOvrdPenBack(
				viewportHandle : HANDLE;
				layerHandle    : HANDLE;
				VAR colorRV    : LONGINT;
				VAR colorGV    : LONGINT;
				VAR colorBV    : LONGINT);
```

```python
def vs.GetVPLrOvrdPenBack(viewportHandle, layerHandle):
    return (colorRV, colorGV, colorBV)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|layerHandle|HANDLE|The layer handle.|
|colorRV|LONGINT|Red value (0-65535)|
|colorGV|LONGINT|Green value (0-65535)|
|colorBV|LONGINT|Blue value (0-65535)|

## Examples
```pascal
GetVPLrOvrdPenBack(viewportHandle, layerHandle, 1, 2, 3);
```
```python
import vs

# Gets the pen background color from a layer override.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
layerHandle = vs.ActLayer()  # handle to the active design layer

colorRV, colorGV, colorBV = vs.GetVPLrOvrdPenBack(viewportHandle, layerHandle)
vs.Message('GetVPLrOvrdPenBack returned: ' + str((colorRV, colorGV, colorBV)))
```

## See Also
VS Functions:
[SetVPLrOvrdPenBack](SetVPLrOvrdPenBack.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
