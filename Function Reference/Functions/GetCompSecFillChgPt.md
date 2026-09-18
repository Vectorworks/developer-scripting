# GetCompSecFillChgPt

## Description
Gets the wall associated section fill change point of a component in an object.

```pascal
FUNCTION GetCompSecFillChgPt(
				object                                   : HANDLE;
				componentIndex                           : INTEGER;
				VAR wallAssociatedSectionFillChangePoint : INTEGER): BOOLEAN;
```

```python
def vs.GetCompSecFillChgPt(object, componentIndex):
    return (BOOLEAN, wallAssociatedSectionFillChangePoint)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a roof face, roof, Roof Style, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|wallAssociatedSectionFillChangePoint|INTEGER|Returns the wall associated section fill change point of the component.  0 - Inner face 1 - Outer face of inner component 2 - Inner face of core 3 - Center of core 4 - Outer face of core 5 - Inner face of outer component 6 - None|

## Examples
```pascal
resultOK := GetCompSecFillChgPt(object, 1, 2);
```
```python
import vs

# Gets the wall associated section fill change point of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, wallAssociatedSectionFillChangePoint = vs.GetCompSecFillChgPt(object, componentIndex)
vs.Message('GetCompSecFillChgPt returned: ' + str((ok, wallAssociatedSectionFillChangePoint)))
```

## See Also
VS Functions:
[SetCompSecFillChgPt](SetCompSecFillChgPt.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
