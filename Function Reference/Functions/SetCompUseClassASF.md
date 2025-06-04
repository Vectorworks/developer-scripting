# SetCompUseClassASF

## Description
Sets the use class fill style for alternate section fill flag of a component in an object.

```pascal
FUNCTION SetCompUseClassASF(
				object                                   : HANDLE;
				componentIndex                           : INTEGER;
				useClassFillStyleForAlternateSectionFill : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompUseClassASF(object, componentIndex, useClassFillStyleForAlternateSectionFill):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassFillStyleForAlternateSectionFill|BOOLEAN|Whether or not the component will use class attributes for its alternate section fill.|

## See Also
VS Functions:
[GetCompUseClassASF](GetCompUseClassASF.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
