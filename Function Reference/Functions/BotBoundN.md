# BotBoundN

## Description
Returns the y-coordinate of the bounding box (bottom right corner) of an object matching the search criteria. If more than one object matches the search criteria, the function will return the value of the coordinate of the bottommost matching object found.

```pascal
FUNCTION BotBoundN(c : CRITERIA): REAL;
```

```python
def vs.BotBoundN(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
```pascal
BotBValue:=BotBoundN(N='MyRect');
```

## Version
Availability: from Vectorworks 2012

## Category
* [Criteria](../Categories/Criteria.md)
