# SetComponentPenColors

## Description
Sets the colors of the pens of a component in an object.

```pascal
FUNCTION SetComponentPenColors(
				obj               : HANDLE;
				componentIndex    : INTEGER;
				leftPenForeColor  : INTEGER;
				leftPenBackColor  : INTEGER;
				rightPenForeColor : INTEGER;
				rightPenBackColor : INTEGER): BOOLEAN;
```

```python
def vs.SetComponentPenColors(obj, componentIndex, leftPenForeColor, leftPenBackColor, rightPenForeColor, rightPenBackColor):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|leftPenForeColor|INTEGER|The fore color of the left pen.|
|leftPenBackColor|INTEGER|The back color of the left pen.|
|rightPenForeColor|INTEGER|The fore color of the right pen.|
|rightPenBackColor|INTEGER|The back color of the right pen.|

## See Also
VS Functions:
[GetComponentPenColors](GetComponentPenColors.md)

## Version
Availability: from VectorWorks 2008

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
