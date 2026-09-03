# SetCompUseClassLPW

## Description
Sets the use class pen weight for left pen flag of a component in an object.

```pascal
FUNCTION SetCompUseClassLPW(
				object                      : HANDLE;
				componentIndex              : INTEGER;
				useClassPenWeightForLeftPen : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompUseClassLPW(object, componentIndex, useClassPenWeightForLeftPen):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassPenWeightForLeftPen|BOOLEAN|Whether or not the component will use class attributes for its left pen weight.|

## Examples
```pascal
resultOK := SetCompUseClassLPW(object, 1, TRUE);
```
```python
import vs

# Sets the use class pen weight for left pen flag of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
useClassPenWeightForLeftPen = True

ok = vs.SetCompUseClassLPW(object, componentIndex, useClassPenWeightForLeftPen)
if ok:
    vs.Message('SetCompUseClassLPW succeeded')
else:
    vs.Message('SetCompUseClassLPW failed')
```

## See Also
VS Functions:
[GetCompUseClassLPW](GetCompUseClassLPW.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
