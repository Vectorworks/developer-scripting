# GetComponentPenStyles

## Description
Gets the left and right side pen styles of a component in an object.

```pascal
FUNCTION GetComponentPenStyles(
				obj               : HANDLE;
				componentIndex    : INTEGER;
				VAR leftPenStyle  : INTEGER;
				VAR rightPenStyle : INTEGER): BOOLEAN;
```

```python
def vs.GetComponentPenStyles(obj, componentIndex):
    return (BOOLEAN, leftPenStyle, rightPenStyle)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|leftPenStyle|INTEGER|Returns the pen style of the component's left line.  Positive values for patterns, negative values for dash styles.|
|rightPenStyle|INTEGER|Returns the pen style of the component's right line.  Positive values for patterns, negative values for dash styles.|

## Remarks
*_c_*, 2016.02.04: This doesn't support Line Types: the values returned are faulty. Use [GetCompPenStylesN](GetCompPenStylesN.md)

## See Also
VS Functions:
[SetComponentPenStyles](SetComponentPenStyles.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
