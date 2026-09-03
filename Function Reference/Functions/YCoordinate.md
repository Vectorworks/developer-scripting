# YCoordinate

## Description
Returns the Y coordinate of the object relative to the user origin.

```pascal
FUNCTION YCoordinate(c : CRITERIA): REAL;
```

```python
def vs.YCoordinate(c):
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
resultVal := YCoordinate(c);
```
```python
import vs

# Returns the Y coordinate of the object relative to the user origin.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

value = vs.YCoordinate(c)
vs.Message('YCoordinate returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Criteria](../Categories/Criteria.md)
