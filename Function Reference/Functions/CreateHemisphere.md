# CreateHemisphere

## Description
Function CreateHemisphere creates a new hemisphere object in a VectorWorks document.

```pascal
FUNCTION CreateHemisphere(
				centerX,centerY,centerZ : REAL;
				topX,topY,topZ          : REAL): HANDLE;
```

```python
def vs.CreateHemisphere(center, top):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|center|REAL|Center point of hemisphere.|
|top|REAL|Top point of hemisphere.|

## Remarks
[sd 8/18/98]

## Examples
```pascal
resultH := CreateHemisphere(1.0, 2.0, 0.5, 1.5, 3.0, 1.0);
```
```python
import vs

# Function CreateHemisphere creates a new hemisphere object in a VectorWorks
# document.
center = (0, 0)
top = (2, 2)

objHandle = vs.CreateHemisphere(center, top)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
