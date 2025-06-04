# SetVPClOvrdPenFore

## Description
Sets the pen foreground color of a class override in a viewport. The color is specified by RGB values in the range 0~65535.

```pascal
PROCEDURE SetVPClOvrdPenFore(
				viewportHandle : HANDLE;
				className      : STRING;
				colorRV        : LONGINT;
				colorGV        : LONGINT;
				colorBV        : LONGINT);
```

```python
def vs.SetVPClOvrdPenFore(viewportHandle, className, colorRV, colorGV, colorBV):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|className|STRING|The name of the class.|
|colorRV|LONGINT|Red color value.|
|colorGV|LONGINT|Green color value.|
|colorBV|LONGINT|Blue color value.|

## See Also
VS Functions:
[GetVPClOvrdPenBack](GetVPClOvrdPenBack.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
