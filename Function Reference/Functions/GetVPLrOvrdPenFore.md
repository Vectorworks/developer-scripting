# GetVPLrOvrdPenFore

## Description
Gets the pen foreground color from a layer override.

```pascal
PROCEDURE GetVPLrOvrdPenFore(
				viewportHandle : HANDLE;
				layerHandle    : HANDLE;
				VAR colorRV    : LONGINT;
				VAR colorGV    : LONGINT;
				VAR colorBV    : LONGINT);
```

```python
def vs.GetVPLrOvrdPenFore(viewportHandle, layerHandle):
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

## See Also
VS Functions:
[SetVPLrOvrdPenFore](SetVPLrOvrdPenFore.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
