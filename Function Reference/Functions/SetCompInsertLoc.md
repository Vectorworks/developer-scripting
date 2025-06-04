# SetCompInsertLoc

## Description
Sets the component insert location of the object.

```pascal
PROCEDURE SetCompInsertLoc(
				object         : HANDLE;
				insertLocation : INTEGER);
```

```python
def vs.SetCompInsertLoc(object, insertLocation):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, Wall Style, or the Wall Preferences.|
|insertLocation|INTEGER|The component insert location of the object. 0 - None 1 - Left 2 - Center 3 - Right|

## See Also
VS Functions:
[GetCompInsertLoc](GetCompInsertLoc.md)

## Version
Availability: from Vectorworks 2023

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
