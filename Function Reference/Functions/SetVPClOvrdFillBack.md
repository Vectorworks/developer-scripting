# SetVPClOvrdFillBack

## Description
Sets the fill background color of a class override in a viewport. The color is specified by RGB values in the range 0~65535.

```pascal
PROCEDURE SetVPClOvrdFillBack(
				viewportHandle : HANDLE;
				className      : STRING;
				colorRV        : LONGINT;
				colorGV        : LONGINT;
				colorBV        : LONGINT);
```

```python
def vs.SetVPClOvrdFillBack(viewportHandle, className, colorRV, colorGV, colorBV):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|className|STRING|The name of the class to override.|
|colorRV|LONGINT|Red color value.|
|colorGV|LONGINT|Green color value.|
|colorBV|LONGINT|Blue color value.|

## Examples
```pascal
SetVPClOvrdFillBack(viewportHandle, 'Wall', 1, 2, 3);
```
```python
import vs

# Sets the fill background color of a class override in a viewport.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'
colorRV = 5
colorGV = 5
colorBV = 5

vs.SetVPClOvrdFillBack(viewportHandle, className, colorRV, colorGV, colorBV)
```

## See Also
VS Functions:
[GetVPClOvrdFillBack](GetVPClOvrdFillBack.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
