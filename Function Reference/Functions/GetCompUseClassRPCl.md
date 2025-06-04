# GetCompUseClassRPCl

## Description
Gets the use class pen colors for right pen flag of a component in an object.

```pascal
FUNCTION GetCompUseClassRPCl(
				object                           : HANDLE;
				componentIndex                   : INTEGER;
				VAR useClassPenColorsForRightPen : BOOLEAN): BOOLEAN;
```

```python
def vs.GetCompUseClassRPCl(object, componentIndex):
    return (BOOLEAN, useClassPenColorsForRightPen)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassPenColorsForRightPen|BOOLEAN|Returns whether or not the component is using class attributes for its right pen colors.|

## See Also
VS Functions:
[SetCompUseClassRPCl](SetCompUseClassRPCl.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
