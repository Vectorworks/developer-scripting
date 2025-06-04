# GetCompUseClassFill

## Description
Gets the use class fill style for fill flag of a component in an object.

```pascal
FUNCTION GetCompUseClassFill(
				object                       : HANDLE;
				componentIndex               : INTEGER;
				VAR useClassFillStyleForFill : BOOLEAN): BOOLEAN;
```

```python
def vs.GetCompUseClassFill(object, componentIndex):
    return (BOOLEAN, useClassFillStyleForFill)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassFillStyleForFill|BOOLEAN|Returns whether or not the component is using class attributes for its fill.|

## See Also
VS Functions:
[SetCompUseClassFill](SetCompUseClassFill.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
