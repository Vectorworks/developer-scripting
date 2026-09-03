# CreateCone

## Description
Creates a 3D cone object in a VectorWorks document.

```pascal
FUNCTION CreateCone(
				centerX,centerY,centerZ : REAL;
				tipX,tipY,tipZ          : REAL;
				radiusDistance          : REAL): HANDLE;
```

```python
def vs.CreateCone(center, tip, radiusDistance):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|center|REAL|Center point of cone.|
|tip|REAL|Tip point of cone.|
|radiusDistance|REAL|Radius of cone base.|

## Remarks
[sd 8/18/98]

## Examples
```pascal
resultH := CreateCone(1.0, 2.0, 0.5, 1.5, 3.0, 1.0, 2.0);
```
```python
import vs

# Creates a 3D cone object in a VectorWorks document.
center = (0, 0)
tip = 'Example'
radiusDistance = 1.0

objHandle = vs.CreateCone(center, tip, radiusDistance)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
