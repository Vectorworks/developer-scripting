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

## See Also
VS Functions:
[SetVPLrOvrdFillBack](SetVPLrOvrdFillBack.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
