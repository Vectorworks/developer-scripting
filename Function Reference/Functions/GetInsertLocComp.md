# GetInsertLocComp

## Description
Gets the insert location component of the object.

```pascal
FUNCTION GetInsertLocComp(object : HANDLE): INTEGER;
```

```python
def vs.GetInsertLocComp(object):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, Wall Style, or the Wall Preferences.|

## Examples
```pascal
resultN := GetInsertLocComp(object);
```
```python
import vs

# Gets the insert location component of the object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetInsertLocComp(object)
vs.Message('GetInsertLocComp returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetInsertLocComp](SetInsertLocComp.md)

## Version
Availability: from Vectorworks 2023

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
