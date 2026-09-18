# GetVPClOvrdFillBack

## Description
Fetches the fill background color of the class override. The color is returned as three RGB components in the range 0~65535.

```pascal
PROCEDURE GetVPClOvrdFillBack(
				viewportHandle : HANDLE;
				className      : STRING;
				VAR colorRV    : LONGINT;
				VAR colorGV    : LONGINT;
				VAR colorBV    : LONGINT);
```

```python
def vs.GetVPClOvrdFillBack(viewportHandle, className):
    return (colorRV, colorGV, colorBV)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|Handle to the viewport.|
|className|STRING|Name of class.|
|colorRV|LONGINT|Returns red color component.|
|colorGV|LONGINT|Returns green color component.|
|colorBV|LONGINT|Returns blue color component.|

## Examples
```pascal
GetVPClOvrdFillBack(viewportHandle, 'Wall', 1, 2, 3);
```
```python
import vs

# Fetches the fill background color of the class override.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'

colorRV, colorGV, colorBV = vs.GetVPClOvrdFillBack(viewportHandle, className)
vs.Message('GetVPClOvrdFillBack returned: ' + str((colorRV, colorGV, colorBV)))
```

## See Also
VS Functions:
[SetVPClOvrdFillBack](SetVPClOvrdFillBack.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
