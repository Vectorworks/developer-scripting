# SurfaceAreaN

## Description
Returns the surface area of the items matching the specified criteria. If more than one object matches the search criteria, the sum of all the surface areas of the matching objects will be returned. <BR>
<BR>
SurfaceAreaN will only return areas on objects which support the solids modelling functions.

```pascal
FUNCTION SurfaceAreaN(c : CRITERIA): REAL;
```

```python
def vs.SurfaceAreaN(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
```pascal
totalArea:=SurfaceAreaN((C='Empty Space'));
```

## Version
Availability: from Vectorworks 2012

## Category
* [Criteria](../Categories/Criteria.md)
