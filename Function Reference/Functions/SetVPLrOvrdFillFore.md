# SetVPLrOvrdFillFore

## Description
Sets the fill foreground color for a layer override.

```pascal
PROCEDURE SetVPLrOvrdFillFore(
				viewportHandle : HANDLE;
				layerHandle    : HANDLE;
				colorRV        : LONGINT;
				colorGV        : LONGINT;
				colorBV        : LONGINT);
```

```python
def vs.SetVPLrOvrdFillFore(viewportHandle, layerHandle, colorRV, colorGV, colorBV):
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

## See Also
VS Functions:
[GetVPLrOvrdFillFore](GetVPLrOvrdFillFore.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
