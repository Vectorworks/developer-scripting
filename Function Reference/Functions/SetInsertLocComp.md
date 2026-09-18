# SetInsertLocComp

## Description
Sets the insert location component of the object.

```pascal
PROCEDURE SetInsertLocComp(
				object         : HANDLE;
				componentIndex : INTEGER);
```

```python
def vs.SetInsertLocComp(object, componentIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the insert location component.|

## Examples
```pascal
SetInsertLocComp(object, 1);
```
```python
import vs

# Sets the insert location component of the object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

vs.SetInsertLocComp(object, componentIndex)
```

## See Also
VS Functions:
[GetInsertLocComp](GetInsertLocComp.md)

## Version
Availability: from Vectorworks 2023

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
