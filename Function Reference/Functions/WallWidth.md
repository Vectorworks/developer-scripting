# WallWidth

## Description
Function WallWidth returns the wall width of the referenced wall object.

```pascal
FUNCTION WallWidth(wallHd : HANDLE): REAL;
```

```python
def vs.WallWidth(wallHd):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wallHd|HANDLE|Handle to wall.|

## Remarks
"Function WallWidth returns the wall width of the referenced wall object", whereas [[VS:HWallWidth]] changes the width of the referenced wall. [[VS:GetWallThickness|GetWallThickness]](wallHandle, thicknessDist) 

(http://www.nemetschek.net/support/custom/vscript/reference/asp/main.asp?name=GetWallThickness) does the same as WallWidth, but is often more practical and at least looks better in scripts.

## See Also
VS Functions:
[GetWallThickness](GetWallThickness.md) 
| [HWallWidth](HWallWidth.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
