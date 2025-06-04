# GetCompUseClassRPS

## Description
Gets the use class pen style for right pen flag of a component in an object.

```pascal
FUNCTION GetCompUseClassRPS(
				object                          : HANDLE;
				componentIndex                  : INTEGER;
				VAR useClassPenStyleForRightPen : BOOLEAN): BOOLEAN;
```

```python
def vs.GetCompUseClassRPS(object, componentIndex):
    return (BOOLEAN, useClassPenStyleForRightPen)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassPenStyleForRightPen|BOOLEAN|Returns whether or not the component is using class attributes for its right pen style.|

## See Also
VS Functions:
[SetCompUseClassRPS](SetCompUseClassRPS.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
