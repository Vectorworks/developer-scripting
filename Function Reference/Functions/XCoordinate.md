# XCoordinate

## Description
Returns the X coordinate of the object relative to the user origin.

```pascal
FUNCTION XCoordinate(c : CRITERIA): REAL;
```

```python
def vs.XCoordinate(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|The search criteria string.|

## Remarks
Valid objects are PIOs, Symbols and Loci.

## Examples
```pascal
resultVal := XCoordinate(c);
```
```python
import vs

# Returns the X coordinate of the object relative to the user origin.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

value = vs.XCoordinate(c)
vs.Message('XCoordinate returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Criteria](../Categories/Criteria.md)
