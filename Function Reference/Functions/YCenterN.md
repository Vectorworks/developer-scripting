# YCenterN

## Description
Returns the y-coordinate of the center point of the bounding box of an object matching the search criteria. If more than one object matches the search criteria, the function will return the y-coordinate of the average center point of all the matching objects

```pascal
FUNCTION YCenterN(c : CRITERIA): REAL;
```

```python
def vs.YCenterN(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
```pascal
YCenValue:=YCenterN(N='Board');
{returns the y-coord of the center of the bounding box of the named object 'Board'
```

```pascal
resultVal := YCenterN(c);
```
```python
import vs

# Returns the y-coordinate of the center point of the bounding box of an
# object matching the search criteria.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

value = vs.YCenterN(c)
vs.Message('YCenterN returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2012

## Category
* [Criteria](../Categories/Criteria.md)
