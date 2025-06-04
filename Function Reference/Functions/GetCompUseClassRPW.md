# GetCompUseClassRPW

## Description
Gets the use class pen weight for right pen flag of a component in an object.

```pascal
FUNCTION GetCompUseClassRPW(
				object                           : HANDLE;
				componentIndex                   : INTEGER;
				VAR useClassPenWeightForRightPen : BOOLEAN): BOOLEAN;
```

```python
def vs.GetCompUseClassRPW(object, componentIndex):
    return (BOOLEAN, useClassPenWeightForRightPen)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassPenWeightForRightPen|BOOLEAN|Returns whether or not the component is using class attributes for its right pen weight.|

## See Also
VS Functions:
[SetCompUseClassRPW](SetCompUseClassRPW.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
