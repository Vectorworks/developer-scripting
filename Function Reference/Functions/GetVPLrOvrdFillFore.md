# GetVPLrOvrdFillFore

## Description
Gets the fill foreground color from a layer override.

```pascal
PROCEDURE GetVPLrOvrdFillFore(
				viewportHandle : HANDLE;
				layerHandle    : HANDLE;
				VAR colorRV    : LONGINT;
				VAR colorGV    : LONGINT;
				VAR colorBV    : LONGINT);
```

```python
def vs.GetVPLrOvrdFillFore(viewportHandle, layerHandle):
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
GetVPLrOvrdFillFore(viewportHandle, layerHandle, 1, 2, 3);
```
```python
import vs

# Gets the fill foreground color from a layer override.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
layerHandle = vs.ActLayer()  # handle to the active design layer

colorRV, colorGV, colorBV = vs.GetVPLrOvrdFillFore(viewportHandle, layerHandle)
vs.Message('GetVPLrOvrdFillFore returned: ' + str((colorRV, colorGV, colorBV)))
```

## See Also
VS Functions:
[SetVPLrOvrdFillFore](SetVPLrOvrdFillFore.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
