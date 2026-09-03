# CreateSphere

## Description
Function CreateSphere creates a new sphere object in a VectorWorks document.

```pascal
FUNCTION CreateSphere(
				centerX,centerY,centerZ : REAL;
				radiusDistance          : REAL): HANDLE;
```

```python
def vs.CreateSphere(center, radiusDistance):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|center|REAL|Center point of sphere.|
|radiusDistance|REAL|Radius of sphere.|

## Remarks
[sd 8/18/98]

## Examples
```pascal
objH1 := CreateSphere (0, 0, 0, 1);
objH1 := ConvertToNURBS (objH1, FALSE);
SetSelect (pluginH);
```
```python
import vs

# Function CreateSphere creates a new sphere object in a VectorWorks document.
center = (0, 0)
radiusDistance = 1.0

objHandle = vs.CreateSphere(center, radiusDistance)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
