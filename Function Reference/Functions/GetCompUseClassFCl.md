# GetCompUseClassFCl

## Description
Gets the use class fill colors for fill flag of a component in an object.

```pascal
FUNCTION GetCompUseClassFCl(
				object                        : HANDLE;
				componentIndex                : INTEGER;
				VAR useClassFillColorsForFill : BOOLEAN): BOOLEAN;
```

```python
def vs.GetCompUseClassFCl(object, componentIndex):
    return (BOOLEAN, useClassFillColorsForFill)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassFillColorsForFill|BOOLEAN|Returns whether or not the component is using class attributes for its fill colors.|

## See Also
VS Functions:
[SetCompUseClassFCl](SetCompUseClassFCl.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
