# GetObjectHiddenLine

## Description
Create lines representing the hidden line geometry of the specified object.

```pascal
FUNCTION GetObjectHiddenLine(
				hGeometry3D      : HANDLE;
				cuttingHeight    : REAL;
				bottomOfCutPlane : BOOLEAN): HANDLE;
```

```python
def vs.GetObjectHiddenLine(hGeometry3D, cuttingHeight, bottomOfCutPlane):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hGeometry3D|HANDLE|   |
|cuttingHeight|REAL|   |
|bottomOfCutPlane|BOOLEAN|   |

## Examples
```pascal
resultH := GetObjectHiddenLine(hGeometry3D, 1.0, TRUE);
```
```python
import vs

# Create lines representing the hidden line geometry of the specified object.
hGeometry3D = vs.FSActLayer()  # handle to the first selected object on the active layer
cuttingHeight = 2.0
bottomOfCutPlane = True

objHandle = vs.GetObjectHiddenLine(hGeometry3D, cuttingHeight, bottomOfCutPlane)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
