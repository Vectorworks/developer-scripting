# SetPrefRGB

## Description
Procedure SetPrefRGB return the RGB color components of the specified preference item. The color must be specified using the RGB components of the desired color. The RGB values are in the range of 0 - 65535.

```pascal
PROCEDURE SetPrefRGB(
				prefIndex : INTEGER;
				colorRV   : LONGINT;
				colorGV   : LONGINT;
				colorBV   : LONGINT);
```

```python
def vs.SetPrefRGB(prefIndex, colorRV, colorGV, colorBV):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|prefIndex|INTEGER|   |
|colorRV|LONGINT|The RGB color component (red).|
|colorGV|LONGINT|The RGB color component (green).|
|colorBV|LONGINT|The RGB color component (blue).|

## See Also
[GetPrefRGB](GetPrefRGB.md)

## Version
Availability: from Vectorworks14.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
