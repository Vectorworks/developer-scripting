# ZCoordinate

## Description
Returns the Z coordinate of the object relative to the object's layer plane.

```pascal
FUNCTION ZCoordinate(c : CRITERIA): REAL;
```

```python
def vs.ZCoordinate(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|The search criteria string.|

## Remarks
Valid objects are PIOs, Symbols and Loci

## Examples
```pascal
resultVal := ZCoordinate(c);
```
```python
import vs

# Returns the Z coordinate of the object relative to the object's layer plane.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

value = vs.ZCoordinate(c)
vs.Message('ZCoordinate returned: ' + str(value))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Criteria](../Categories/Criteria.md)
