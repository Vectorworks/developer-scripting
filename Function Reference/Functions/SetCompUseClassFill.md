# SetCompUseClassFill

## Description
Sets the use class fill style for fill flag of a component in an object.

```pascal
FUNCTION SetCompUseClassFill(
				object                   : HANDLE;
				componentIndex           : INTEGER;
				useClassFillStyleForFill : BOOLEAN): BOOLEAN;
```

```python
def vs.SetCompUseClassFill(object, componentIndex, useClassFillStyleForFill):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassFillStyleForFill|BOOLEAN|Whether or not the component will use class attributes for its fill.|

## Examples
```pascal
resultOK := SetCompUseClassFill(object, 1, TRUE);
```
```python
import vs

# Sets the use class fill style for fill flag of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
useClassFillStyleForFill = True

ok = vs.SetCompUseClassFill(object, componentIndex, useClassFillStyleForFill)
if ok:
    vs.Message('SetCompUseClassFill succeeded')
else:
    vs.Message('SetCompUseClassFill failed')
```

## See Also
VS Functions:
[GetCompUseClassFill](GetCompUseClassFill.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
