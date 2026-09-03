# SetCompUseClassASFCl

## Description
Sets the use class fill colors for alternate section fill flag of a component in an object.

```pascal
FUNCTION SetCompUseClassASFCl(
				object                                    : HANDLE;
				componentIndex                            : INTEGER;
				useClassFillColorsForAlternateSectionFill : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompUseClassASFCl(object, componentIndex, useClassFillColorsForAlternateSectionFill):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassFillColorsForAlternateSectionFill|BOOLEAN|Whether or not the component will use class attributes for its alternate section fill colors.|

## Examples
```pascal
resultOK := SetCompUseClassASFCl(object, 1, TRUE);
```
```python
import vs

# Sets the use class fill colors for alternate section fill flag of a
# component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
useClassFillColorsForAlternateSectionFill = True

ok = vs.SetCompUseClassASFCl(object, componentIndex, useClassFillColorsForAlternateSectionFill)
if ok:
    vs.Message('SetCompUseClassASFCl succeeded')
else:
    vs.Message('SetCompUseClassASFCl failed')
```

## See Also
VS Functions:
[GetCompUseClassASFCl](GetCompUseClassASFCl.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
