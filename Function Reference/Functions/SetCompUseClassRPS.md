# SetCompUseClassRPS

## Description
Sets the use class pen style for right pen flag of a component in an object.

```pascal
FUNCTION SetCompUseClassRPS(
				object                      : HANDLE;
				componentIndex              : INTEGER;
				useClassPenStyleForRightPen : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompUseClassRPS(object, componentIndex, useClassPenStyleForRightPen):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassPenStyleForRightPen|BOOLEAN|Whether or not the component will use class attributes for its right pen style.|

## See Also
VS Functions:
[GetCompUseClassRPS](GetCompUseClassRPS.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
