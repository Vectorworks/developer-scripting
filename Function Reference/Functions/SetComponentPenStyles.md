# SetComponentPenStyles

## Description
Sets the left and right pen styles for a component in an object.

```pascal
FUNCTION SetComponentPenStyles(
				obj            : HANDLE;
				componentIndex : INTEGER;
				leftPenStyle   : INTEGER;
				rightPenStyle  : INTEGER): BOOLEAN;
```

```python
def vs.SetComponentPenStyles(obj, componentIndex, leftPenStyle, rightPenStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|leftPenStyle|INTEGER|The pen style of the component's left line.  Positive values for patterns, negative values for dash styles.|
|rightPenStyle|INTEGER|The pen style of the component's right line.  Positive values for patterns, negative values for dash styles.|

## See Also
VS Functions:
[GetComponentPenStyles](GetComponentPenStyles.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
