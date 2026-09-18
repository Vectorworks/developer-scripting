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

## Examples
```pascal
resultOK := PlanarPtTo3DModelPt(1, 1.0, 2.0);
```
```python
import vs

# Transform a 2D point on the specified plane into a 3D point.
refID = 1
pt2D = 1.0

ok, outPt3D = vs.PlanarPtTo3DModelPt(refID, pt2D)
vs.Message('PlanarPtTo3DModelPt returned: ' + str((ok, outPt3D)))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Utility](../Categories/Utility.md)
