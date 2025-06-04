# GetCompUseClassASF

## Description
Gets the use class fill style for alternate section fill flag of a component in an object.

```pascal
FUNCTION GetCompUseClassASF(
				object                                       : HANDLE;
				componentIndex                               : INTEGER;
				VAR useClassFillStyleForAlternateSectionFill : BOOLEAN): BOOLEAN;
```

```python
def vs.GetCompUseClassASF(object, componentIndex):
    return (BOOLEAN, useClassFillStyleForAlternateSectionFill)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassFillStyleForAlternateSectionFill|BOOLEAN|Returns whether or not the component is using class attributes for its alternate section fill.|

## See Also
VS Functions:
[SetCompUseClassASF](SetCompUseClassASF.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
