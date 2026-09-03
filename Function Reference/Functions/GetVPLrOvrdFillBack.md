# GetVPLrOvrdFillBack

## Description
Gets the fill background color from a layer override.

```pascal
PROCEDURE GetVPLrOvrdFillBack(
				viewportHandle : HANDLE;
				layerHandle    : HANDLE;
				VAR colorRV    : LONGINT;
				VAR colorGV    : LONGINT;
				VAR colorBV    : LONGINT);
```

```python
def vs.GetVPLrOvrdFillBack(viewportHandle, layerHandle):
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
GetVPLrOvrdFillBack(viewportHandle, layerHandle, 1, 2, 3);
```
```python
import vs

# Gets the fill background color from a layer override.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
layerHandle = vs.ActLayer()  # handle to the active design layer

colorRV, colorGV, colorBV = vs.GetVPLrOvrdFillBack(viewportHandle, layerHandle)
vs.Message('GetVPLrOvrdFillBack returned: ' + str((colorRV, colorGV, colorBV)))
```

## See Also
VS Functions:
[SetVPLrOvrdFillBack](SetVPLrOvrdFillBack.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
