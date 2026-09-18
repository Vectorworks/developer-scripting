# SetCompAltSecFillCl

## Description
Sets the alternate section fill colors of a component in an object.

```pascal
FUNCTION SetCompAltSecFillCl(
				object                        : HANDLE;
				componentIndex                : INTEGER;
				alternateSectionFillForeColor : INTEGER;
				alternateSectionFillBackColor : INTEGER): BOOLEAN;
```

```python
def vs.SetCompAltSecFillCl(object, componentIndex, alternateSectionFillForeColor, alternateSectionFillBackColor):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|alternateSectionFillForeColor|INTEGER|The alternate section fill fore color of the component.|
|alternateSectionFillBackColor|INTEGER|The alternate section fill back color of the component.|

## Examples
```pascal
resultOK := SetCompAltSecFillCl(object, 1, 2, 3);
```
```python
import vs

# Sets the alternate section fill colors of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
alternateSectionFillForeColor = 5
alternateSectionFillBackColor = 5

ok = vs.SetCompAltSecFillCl(object, componentIndex, alternateSectionFillForeColor, alternateSectionFillBackColor)
if ok:
    vs.Message('SetCompAltSecFillCl succeeded')
else:
    vs.Message('SetCompAltSecFillCl failed')
```

## See Also
VS Functions:
[GetCompAltSecFillCl](GetCompAltSecFillCl.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
