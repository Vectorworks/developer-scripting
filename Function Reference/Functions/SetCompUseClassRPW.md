# SetCompUseClassRPW

## Description
Sets the use class pen weight for right pen flag of a component in an object.

```pascal
FUNCTION SetCompUseClassRPW(
				object                       : HANDLE;
				componentIndex               : INTEGER;
				useClassPenWeightForRightPen : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompUseClassRPW(object, componentIndex, useClassPenWeightForRightPen):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassPenWeightForRightPen|BOOLEAN|Whether or not the component will use class attributes for its right pen weight.|

## See Also
VS Functions:
[GetCompUseClassRPW](GetCompUseClassRPW.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
