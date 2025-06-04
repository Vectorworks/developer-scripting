# SetCompUseClassFCl

## Description
Sets the use class fill colors for fill flag of a component in an object.

```pascal
FUNCTION SetCompUseClassFCl(
				object                    : HANDLE;
				componentIndex            : INTEGER;
				useClassFillColorsForFill : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompUseClassFCl(object, componentIndex, useClassFillColorsForFill):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassFillColorsForFill|BOOLEAN|Whether or not the component will use class attributes for its fill colors.|

## See Also
VS Functions:
[GetCompUseClassFCl](GetCompUseClassFCl.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
