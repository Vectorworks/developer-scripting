# GetCompInsertLoc

## Description
Gets the component insert location of the object.

```pascal
FUNCTION GetCompInsertLoc(object : HANDLE): INTEGER;
```

```python
def vs.GetCompInsertLoc(object):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, Wall Style, or the Wall Preferences.|

## Examples
```pascal
resultN := GetCompInsertLoc(object);
```
```python
import vs

# Gets the component insert location of the object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetCompInsertLoc(object)
vs.Message('GetCompInsertLoc returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetCompInsertLoc](SetCompInsertLoc.md)

## Version
Availability: from Vectorworks 2023

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
