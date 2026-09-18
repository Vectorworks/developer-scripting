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

```pascal
resultVal := BotBoundN(c);
```
```python
import vs

# Returns the y-coordinate of the bounding box (bottom right corner) of an
# object matching the search criteria.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

value = vs.BotBoundN(c)
vs.Message('BotBoundN returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2012

## Category
* [Criteria](../Categories/Criteria.md)
