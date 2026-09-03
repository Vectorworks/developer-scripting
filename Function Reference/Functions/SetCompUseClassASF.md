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

## Examples
```pascal
resultOK := SetCompUseClassASF(object, 1, TRUE);
```
```python
import vs

# Sets the use class fill style for alternate section fill flag of a
# component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
useClassFillStyleForAlternateSectionFill = True

ok = vs.SetCompUseClassASF(object, componentIndex, useClassFillStyleForAlternateSectionFill)
if ok:
    vs.Message('SetCompUseClassASF succeeded')
else:
    vs.Message('SetCompUseClassASF failed')
```

## See Also
VS Functions:
[GetCompUseClassASF](GetCompUseClassASF.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
