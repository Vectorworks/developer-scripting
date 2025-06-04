# GetWallHoleTexturePart

## Description
Gets the wall texture part of an object in the wall hole group of a symbol definition or plug-in object.  This is the wall texture part given to faces of the wall that are created by cutting a hole in the wall with the object.

```pascal
FUNCTION GetWallHoleTexturePart(obj : HANDLE): INTEGER;
```

```python
def vs.GetWallHoleTexturePart(obj):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The handle to the cutting object in the wall hole group of a symbol definition or plug-in object.|

## See Also
VS Functions:
[SetWallHoleTexturePart](SetWallHoleTexturePart.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Textures](../Categories/Textures.md)
