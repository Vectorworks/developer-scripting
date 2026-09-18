# SetVPLrOvrdPenBack

## Description
Sets the pen background color for a layer override.

```pascal
PROCEDURE SetVPLrOvrdPenBack(
				viewportHandle : HANDLE;
				layerHandle    : HANDLE;
				colorRV        : LONGINT;
				colorGV        : LONGINT;
				colorBV        : LONGINT);
```

```python
def vs.SetVPLrOvrdPenBack(viewportHandle, layerHandle, colorRV, colorGV, colorBV):
    return None
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
SetVPLrOvrdPenBack(viewportHandle, layerHandle, 1, 2, 3);
```
```python
import vs

# Sets the pen background color for a layer override.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
layerHandle = vs.ActLayer()  # handle to the active design layer
colorRV = 5
colorGV = 5
colorBV = 5

vs.SetVPLrOvrdPenBack(viewportHandle, layerHandle, colorRV, colorGV, colorBV)
```

## See Also
VS Functions:
[GetVPLrOvrdPenBack](GetVPLrOvrdPenBack.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
