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

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
