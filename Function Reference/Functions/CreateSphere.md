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

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
