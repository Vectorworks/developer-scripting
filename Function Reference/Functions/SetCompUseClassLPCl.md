# SetCompUseClassLPCl

## Description
Sets the use class pen colors for left pen flag of a component in an object.

```pascal
FUNCTION SetCompUseClassLPCl(
				object                      : HANDLE;
				componentIndex              : INTEGER;
				useClassPenColorsForLeftPen : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompUseClassLPCl(object, componentIndex, useClassPenColorsForLeftPen):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassPenColorsForLeftPen|BOOLEAN|Whether or not the component will use class attributes for its left pen colors.|

## Examples
```pascal
resultOK := SetCompUseClassLPCl(object, 1, TRUE);
```
```python
import vs

# Sets the use class pen colors for left pen flag of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
useClassPenColorsForLeftPen = True

ok = vs.SetCompUseClassLPCl(object, componentIndex, useClassPenColorsForLeftPen)
if ok:
    vs.Message('SetCompUseClassLPCl succeeded')
else:
    vs.Message('SetCompUseClassLPCl failed')
```

## See Also
VS Functions:
[GetCompUseClassLPCl](GetCompUseClassLPCl.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
