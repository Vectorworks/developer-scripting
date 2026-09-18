# GetCompPenStylesN

## Description
Gets the pen styles of a component in an object.

```pascal
FUNCTION GetCompPenStylesN(
				object            : HANDLE;
				componentIndex    : INTEGER;
				VAR leftPenStyle  : LONGINT;
				VAR rightPenStyle : LONGINT): BOOLEAN;
```

```python
def vs.GetCompPenStylesN(object, componentIndex):
    return (BOOLEAN, leftPenStyle, rightPenStyle)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|leftPenStyle|LONGINT|Returns the left pen style of the component.|
|rightPenStyle|LONGINT|Returns the right pen style of the component.|

## Examples
```pascal
resultOK := GetCompPenStylesN(object, 1, 2, 3);
```
```python
import vs

# Gets the pen styles of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, leftPenStyle, rightPenStyle = vs.GetCompPenStylesN(object, componentIndex)
vs.Message('GetCompPenStylesN returned: ' + str((ok, leftPenStyle, rightPenStyle)))
```

## See Also
VS Functions:
[SetCompPenStylesN](SetCompPenStylesN.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
