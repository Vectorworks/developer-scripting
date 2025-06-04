# PlanarPtTo3DModelPt

## Description
Transform a 2D point on the specified plane into a 3D point.

```pascal
FUNCTION PlanarPtTo3DModelPt(
				refID       : LONGINT;
				pt2D        : REAL;
				VAR outPt3D : REAL): BOOLEAN;
```

```python
def vs.PlanarPtTo3DModelPt(refID, pt2D):
    return (BOOLEAN, outPt3D)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|refID|LONGINT|Reference ID of the plane.|
|pt2D|REAL|The 2D point on the specified plane.|
|outPt3D|REAL|Output. The resulted 3D point.|

## Version
Availability: from Vectorworks 2011

## Category
* [Utility](../Categories/Utility.md)
