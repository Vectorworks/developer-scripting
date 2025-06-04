# TopBoundN

## Description
Returns the y-coordinate of the bounding box (top left corner) of an object matching the search criteria. If more than one object matches the search criteria, the function will return the value of the coordinate of the topmost matching object found.

```pascal
FUNCTION TopBoundN(c : CRITERIA): REAL;
```

```python
def vs.TopBoundN(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
```pascal
TopBValue:=TopBoundN(N='MyRect');
```

## Version
Availability: from Vectorworks 2012

## Category
* [Criteria](../Categories/Criteria.md)
