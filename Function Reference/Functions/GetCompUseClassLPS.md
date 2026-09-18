# GetCompUseClassLPS

## Description
Gets the use class pen style for left pen flag of a component in an object.

```pascal
FUNCTION GetCompUseClassLPS(
				object                         : HANDLE;
				componentIndex                 : INTEGER;
				VAR useClassPenStyleForLeftPen : BOOLEAN): BOOLEAN;
```

```python
def vs.GetCompUseClassLPS(object, componentIndex):
    return (BOOLEAN, useClassPenStyleForLeftPen)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|useClassPenStyleForLeftPen|BOOLEAN|Returns whether or not the component is using class attributes for its left pen style.|

## Examples
```pascal
resultOK := GetCompUseClassLPS(object, 1, TRUE);
```
```python
import vs

# Gets the use class pen style for left pen flag of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, useClassPenStyleForLeftPen = vs.GetCompUseClassLPS(object, componentIndex)
vs.Message('GetCompUseClassLPS returned: ' + str((ok, useClassPenStyleForLeftPen)))
```

## See Also
VS Functions:
[SetCompUseClassLPS](SetCompUseClassLPS.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
