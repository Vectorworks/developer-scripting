# GetPlantToolPlantName

## Description
Returns the name of the current plant that is stored in the plant tool.

```pascal
FUNCTION GetPlantToolPlantName : STRING;
```

```python
def vs.GetPlantToolPlantName():
    return STRING
```

## Examples
```pascal
resultStr := GetPlantToolPlantName;
```
```python
import vs

# Returns the name of the current plant that is stored in the plant tool.
name = vs.GetPlantToolPlantName()
vs.Message('GetPlantToolPlantName returned: ' + str(name))
```

## Version
Availability: from VectorWorks13.0

## Category
* [Utility](../Categories/Utility.md)
