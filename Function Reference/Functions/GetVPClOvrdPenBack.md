# GetVPClOvrdPenBack

## Description
Fetches the pen background color of the class override. The color is returned as three RGB components in the range 0~65535.

```pascal
PROCEDURE GetVPClOvrdPenBack(
				viewportHandle : HANDLE;
				className      : STRING;
				VAR colorRV    : LONGINT;
				VAR colorGV    : LONGINT;
				VAR colorBV    : LONGINT);
```

```python
def vs.GetVPClOvrdPenBack(viewportHandle, className):
    return (colorRV, colorGV, colorBV)
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
[SetVPClOvrdPenBack](SetVPClOvrdPenBack.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
