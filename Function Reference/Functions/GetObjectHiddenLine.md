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

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
