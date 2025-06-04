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

## See Also
VS Functions:
[GetVPLrOvrdFillBack](GetVPLrOvrdFillBack.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
