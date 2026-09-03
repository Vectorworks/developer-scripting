# SetCompPenStylesN

## Description
Sets the pen styles of a component in an object.

```pascal
FUNCTION SetCompPenStylesN(
				object         : HANDLE;
				componentIndex : INTEGER;
				leftPenStyle   : LONGINT;
				rightPenStyle  : LONGINT): BOOLEAN;
```

```python
def vs.SetCompPenStylesN(object, componentIndex, leftPenStyle, rightPenStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|leftPenStyle|LONGINT|The left pen style of the component.|
|rightPenStyle|LONGINT|The right pen style of the component.|

## Examples
```pascal
resultOK := SetCompPenStylesN(object, 1, 2, 3);
```
```python
import vs

# Sets the pen styles of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
leftPenStyle = 0
rightPenStyle = 0

ok = vs.SetCompPenStylesN(object, componentIndex, leftPenStyle, rightPenStyle)
if ok:
    vs.Message('SetCompPenStylesN succeeded')
else:
    vs.Message('SetCompPenStylesN failed')
```

## See Also
VS Functions:
[GetCompPenStylesN](GetCompPenStylesN.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
