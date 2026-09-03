# GetCompInsertLocOff

## Description
Gets the component insert location offset of the object.

```pascal
FUNCTION GetCompInsertLocOff(object : HANDLE): REAL;
```

```python
def vs.GetCompInsertLocOff(object):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, Wall Style, or the Wall Preferences.|

## Examples
```pascal
resultVal := GetCompInsertLocOff(object);
```
```python
import vs

# Gets the component insert location offset of the object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.GetCompInsertLocOff(object)
vs.Message('GetCompInsertLocOff returned: ' + str(value))
```

## See Also
VS Functions:
[SetCompInsertLocOff](SetCompInsertLocOff.md)

## Version
Availability: from Vectorworks 2023

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
