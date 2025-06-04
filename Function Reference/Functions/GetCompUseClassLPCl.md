# GetCompUseClassLPCl

## Description
Gets the use class pen colors for left pen flag of a component in an object.

```pascal
FUNCTION GetCompUseClassLPCl(
				object                          : HANDLE;
				componentIndex                  : INTEGER;
				VAR useClassPenColorsForLeftPen : BOOLEAN): BOOLEAN;
```

```python
def vs.GetCompUseClassLPCl(object, componentIndex):
    return (BOOLEAN, useClassPenColorsForLeftPen)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassPenColorsForLeftPen|BOOLEAN|Returns whether or not the component is using class attributes for its left pen colors.|

## See Also
VS Functions:
[SetCompUseClassLPCl](SetCompUseClassLPCl.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
