# ObjectType

## Description
Returns the type identifier an object. If more than one object matches the search criteria, the type identifier of the last matching object will be returned.

```pascal
FUNCTION ObjectType(c : CRITERIA): INTEGER;
```

```python
def vs.ObjectType(c):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Examples
VectorScript:
```pascal
TypeValue:=ObjectType(N='Mystery Object');
{returns the type of the object named 'Mystery Object'}
```
Python:
```python
TypeValue = vs.ObjectType( "N='Mystery Object'" );
# returns the type of the object named 'Mystery Object'
```

```pascal
resultN := ObjectType(c);
```
```python
import vs

# Returns the type identifier an object.
c = "(SEL=TRUE)"  # selection criteria - all selected objects

resultN = vs.ObjectType(c)
vs.Message('ObjectType returned: ' + str(resultN))
```

## Version
Availability: from All Versions

## Category
* [Criteria](../Categories/Criteria.md)
