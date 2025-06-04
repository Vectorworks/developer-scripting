# ZCenterN

## Description
Returns the z-coordinate value of the center of the bounding box of an object matching the search criteria. If more than one object matches the search criteria, the function will return the z-coordinate of the average center point of all the matching objects

```pascal
FUNCTION ZCenterN(c : CRITERIA): REAL;
```

```python
def vs.ZCenterN(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
```pascal
ZCenValue:=ZCenterN(N='Board');
{returns the z-coord of the center of the bounding box of the named object 'Board'
```

## Version
Availability: from Vectorworks 2012

## Category
* [Criteria](../Categories/Criteria.md)
