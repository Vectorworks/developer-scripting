# LengthN

## Description
Returns the length of an object. If more than one object matches the search criteria, the function will return the sum of all the matching object lengths.

```pascal
FUNCTION LengthN(c : CRITERIA): REAL;
```

```python
def vs.LengthN(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
```pascal
LengthValue:=LengthN(C='CrossMembers');
{returns the length of all objects in class 'CrossMembers'}
```

```pascal
resultVal := LengthN(c);
```
```python
import vs

# Returns the length of an object.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

distance = vs.LengthN(c)
vs.Message('LengthN returned: ' + str(distance))
```

## Version
Availability: from Vectorworks 2012

## Category
* [Criteria](../Categories/Criteria.md)
