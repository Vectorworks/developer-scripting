# SetVPLrOvrdFillBack

## Description
Sets the fill background color for a layer override.

```pascal
PROCEDURE SetVPLrOvrdFillBack(
				viewportHandle : HANDLE;
				layerHandle    : HANDLE;
				colorRV        : LONGINT;
				colorGV        : LONGINT;
				colorBV        : LONGINT);
```

```python
def vs.SetVPLrOvrdFillBack(viewportHandle, layerHandle, colorRV, colorGV, colorBV):
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
SetVPLrOvrdFillBack(viewportHandle, layerHandle, 1, 2, 3);
```
```python
import vs

# Sets the fill background color for a layer override.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
layerHandle = vs.ActLayer()  # handle to the active design layer
colorRV = 5
colorGV = 5
colorBV = 5

vs.SetVPLrOvrdFillBack(viewportHandle, layerHandle, colorRV, colorGV, colorBV)
```

## See Also
VS Functions:
[GetVPLrOvrdFillBack](GetVPLrOvrdFillBack.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
