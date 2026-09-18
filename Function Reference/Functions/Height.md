# Height

## Description
Returns the height of an object. If more than one object matches the search criteria, the function will return the sum of all the matching object heights.

```pascal
FUNCTION Height(c : CRITERIA): REAL;
```

```python
def vs.Height(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
#### VectorScript ####
```pascal
HeightValue:=Height(N='North Wall');
```
#### Python ####
```python
HeightValue = vs.Height((N='North Wall'))
```

```pascal
resultVal := Height(c);
```
```python
import vs

# Returns the height of an object.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

value = vs.Height(c)
vs.Message('Height returned: ' + str(value))
```

## Version
Availability: from All Versions

## Category
* [Criteria](../Categories/Criteria.md)
