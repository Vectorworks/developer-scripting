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

## See Also
VS Functions:
[SetCompPenStylesN](SetCompPenStylesN.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
