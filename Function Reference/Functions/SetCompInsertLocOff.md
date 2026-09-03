# SetCompInsertLocOff

## Description
Sets the component insert location offset of the object.

```pascal
PROCEDURE SetCompInsertLocOff(
				object               : HANDLE;
				insertLocationOffset : REAL (Coordinate));
```

```python
def vs.SetCompInsertLocOff(object, insertLocationOffset):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, Wall Style, or the Wall Preferences.|
|insertLocationOffset|REAL (Coordinate)|The component insert location offset of the object.|

## Examples
```pascal
SetCompInsertLocOff(object, 1.0);
```
```python
import vs

# Sets the component insert location offset of the object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
insertLocationOffset = 0.0

vs.SetCompInsertLocOff(object, insertLocationOffset)
```

## See Also
VS Functions:
[GetCompInsertLocOff](GetCompInsertLocOff.md)

## Version
Availability: from Vectorworks 2023

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
