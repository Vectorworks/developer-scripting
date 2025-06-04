# SetWallHoleTexturePart

## Description
Sets the wall texture part of an object in the wall hole group of a symbol definition or plug-in object.  This is the wall texture part given to faces of the wall that are created by cutting a hole in the wall with the object.

```pascal
PROCEDURE SetWallHoleTexturePart(
				obj  : HANDLE;
				part : INTEGER);
```

```python
def vs.SetWallHoleTexturePart(obj, part):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The handle to the cutting object in the wall hole group of a symbol definition or plug-in object.|
|part|INTEGER|The wall texture part.||0 - The wall Holes texture part|1 - The wall Left texture part|2 - The wall Right texture part|

## See Also
VS Functions:
[GetWallHoleTexturePart](GetWallHoleTexturePart.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
