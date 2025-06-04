# CriteriaSurfaceArea

## Description
<b>[[VS:Vectorworks 2012 Deprecated Functions|DEPRECATED after Vectorworks2012]]</b>.. See [[VS:SurfaceAreaN|SurfaceAreaN]] for a replacement.

Returns the surface area of the items matching the specified criteria. If more than one object matches the search criteria, the sum of all the surface areas of the matching objects will be returned. 

CriteriaSurfaceArea will return only return areas on objects which support the solids modelling functions.

```pascal
FUNCTION CriteriaSurfaceArea(c : CRITERIA): REAL;
```

```python
def vs.CriteriaSurfaceArea(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Remarks
This function returns the surface area of the items matching the current criteria.  It will return 0 for any objects that will not work with the solids modeling functions.

## Examples
#### VectorScript ####
```pascal
totalArea:=CriteriaSurfaceArea((C='Empty Space'));
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks12.0
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* [Criteria](../Categories/Criteria.md)
