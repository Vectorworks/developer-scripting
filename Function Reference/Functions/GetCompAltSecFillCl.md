# GetCompAltSecFillCl

## Description
Gets the alternate section fill colors of a component in an object.

```pascal
FUNCTION GetCompAltSecFillCl(
				object                            : HANDLE;
				componentIndex                    : INTEGER;
				VAR alternateSectionFillForeColor : INTEGER;
				VAR alternateSectionFillBackColor : INTEGER): BOOLEAN;
```

```python
def vs.GetCompAltSecFillCl(object, componentIndex):
    return (BOOLEAN, alternateSectionFillForeColor, alternateSectionFillBackColor)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|alternateSectionFillForeColor|INTEGER|Returns the alternate section fill fore color of the component.|
|alternateSectionFillBackColor|INTEGER|Returns the alternate section fill back color of the component.|

## Remarks
*\_c\_*: 2016.02.03:  See remarks under [GetCompAltSecFill](GetCompAltSecFill.md)!

## Examples
```pascal
resultOK := GetCompAltSecFillCl(object, 1, 2, 3);
```
```python
import vs

# Gets the alternate section fill colors of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, alternateSectionFillForeColor, alternateSectionFillBackColor = vs.GetCompAltSecFillCl(object, componentIndex)
vs.Message('GetCompAltSecFillCl returned: ' + str((ok, alternateSectionFillForeColor, alternateSectionFillBackColor)))
```

## See Also
VS Functions:
[SetCompAltSecFillCl](SetCompAltSecFillCl.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
