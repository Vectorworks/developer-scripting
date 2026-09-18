# SetCompUseClassLPS

## Description
Sets the use class pen style for left pen flag of a component in an object.

```pascal
FUNCTION SetCompUseClassLPS(
				object                     : HANDLE;
				componentIndex             : INTEGER;
				useClassPenStyleForLeftPen : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompUseClassLPS(object, componentIndex, useClassPenStyleForLeftPen):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassPenStyleForLeftPen|BOOLEAN|Whether or not the component will use class attributes for its left pen style.|

## Examples
```pascal
resultOK := SetCompUseClassLPS(object, 1, TRUE);
```
```python
import vs

# Sets the use class pen style for left pen flag of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
useClassPenStyleForLeftPen = True

ok = vs.SetCompUseClassLPS(object, componentIndex, useClassPenStyleForLeftPen)
if ok:
    vs.Message('SetCompUseClassLPS succeeded')
else:
    vs.Message('SetCompUseClassLPS failed')
```

## See Also
VS Functions:
[GetCompUseClassLPS](GetCompUseClassLPS.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
