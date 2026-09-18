# LeftBoundN

## Description
Returns the x-coordinate of the bounding box (top left corner) of an object matching the search criteria. If more than one object matches the search criteria, the function will return the value of the coordinate of the leftmost matching object found.

```pascal
FUNCTION LeftBoundN(c : CRITERIA): REAL;
```

```python
def vs.LeftBoundN(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
```pascal
LeftBValue:=LeftBoundN(N='MyRect');
```

```pascal
BEGIN
wsPosX := LeftBoundN(SEL);
wsPosY := TopBoundN(SEL);
```
```python
import vs

# Returns the x-coordinate of the bounding box (top left corner) of an object
# matching the search criteria.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

value = vs.LeftBoundN(c)
vs.Message('LeftBoundN returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2012

## Category
* [Criteria](../Categories/Criteria.md)
