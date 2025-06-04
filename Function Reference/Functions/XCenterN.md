# XCenterN

## Description
Returns the x-coordinate of the center point of the bounding box of an object matching the search criteria. If more than one object matches the search criteria, the function will return the x-coordinate of the average center point of all the matching objects

```pascal
FUNCTION XCenterN(c : CRITERIA): REAL;
```

```python
def vs.XCenterN(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
```pascal
XCenValue:=XCenterN(N='Board');
{returns the x-coord of the center of the bounding box the named object 'Board'
```

## Version
Availability: from Vectorworks 2012

## Category
* [Criteria](../Categories/Criteria.md)
