# AreaN

## Description
Returns the area of an object. If more than one object matches the search criteria, the function will return the sum of all the matching object areas.

```pascal
FUNCTION AreaN(c : CRITERIA): REAL;
```

```python
def vs.AreaN(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
```pascal
totalA:=AreaN((C='Plywood'));
{returns the area of all objects in class 'Plywood'}
```

## Version
Availability: from Vectorworks 2012

## Category
* [Criteria](../Categories/Criteria.md)
