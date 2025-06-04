# GetCompUseClassLPW

## Description
Gets the use class pen weight for left pen flag of a component in an object.

```pascal
FUNCTION GetCompUseClassLPW(
				object                          : HANDLE;
				componentIndex                  : INTEGER;
				VAR useClassPenWeightForLeftPen : BOOLEAN): BOOLEAN;
```

```python
def vs.GetCompUseClassLPW(object, componentIndex):
    return (BOOLEAN, useClassPenWeightForLeftPen)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassPenWeightForLeftPen|BOOLEAN|Returns whether or not the component is using class attributes for its left pen weight.|

## See Also
VS Functions:
[SetCompUseClassLPW](SetCompUseClassLPW.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
