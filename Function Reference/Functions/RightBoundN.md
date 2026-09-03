# RightBoundN

## Description
Returns the x-coordinate of the bounding box (bottom right corner) of an object matching the search criteria If more than one object matches the search criteria, the function will return the value of the coordinate of the rightmost matching object found.

```pascal
FUNCTION RightBoundN(c : CRITERIA): REAL;
```

```python
def vs.RightBoundN(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
```pascal
RightBValue:=RightBoundN(N='MyRect');
```

```pascal
resultVal := RightBoundN(c);
```
```python
import vs

# Returns the x-coordinate of the bounding box (bottom right corner) of an
# object matching the search criteria If more than one object matches the
# search crite.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

value = vs.RightBoundN(c)
vs.Message('RightBoundN returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2012

## Category
* [Criteria](../Categories/Criteria.md)
