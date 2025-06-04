# SetCompUseClassRPCl

## Description
Sets the use class pen colors for right pen flag of a component in an object.

```pascal
FUNCTION SetCompUseClassRPCl(
				object                       : HANDLE;
				componentIndex               : INTEGER;
				useClassPenColorsForRightPen : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompUseClassRPCl(object, componentIndex, useClassPenColorsForRightPen):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassPenColorsForRightPen|BOOLEAN|Whether or not the component will use class attributes for its right pen colors.|

## See Also
VS Functions:
[GetCompUseClassRPCl](GetCompUseClassRPCl.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
