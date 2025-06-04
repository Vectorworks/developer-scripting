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

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
