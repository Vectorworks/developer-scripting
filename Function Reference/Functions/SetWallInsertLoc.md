# SetWallInsertLoc

## Description
Sets the wall insert location of a symbol definition, plug-in object style, or plug-in object.

```pascal
FUNCTION SetWallInsertLoc(
				hObject        : HANDLE;
				insertLocation : INTEGER): BOOLEAN;
```

```python
def vs.SetWallInsertLoc(hObject, insertLocation):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The symbol definition, plug-in object style, or plug-in object.|
|insertLocation|INTEGER|The wall insert location.  -1 - Insert on the nearest edge of the wall 0 - Insert on the center of the wall 1 - Insert on the left edge of the wall 2 - Insert on the right edge of the wall 3 - Insert on the center of the wall core component 4 - Insert on the left edge of the wall core component 5 - Insert on the right edge of the wall core component|

## See Also
VS Functions:
[GetWallInsertLoc](GetWallInsertLoc.md)

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
