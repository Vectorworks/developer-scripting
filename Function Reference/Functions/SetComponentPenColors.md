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

## Examples
```pascal
resultOK := SetComponentPenColors(obj, 1, 2, 3, 10, 5);
```
```python
import vs

# Sets the colors of the pens of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
leftPenForeColor = 5
leftPenBackColor = 5
rightPenForeColor = 5
rightPenBackColor = 5

ok = vs.SetComponentPenColors(obj, componentIndex, leftPenForeColor, leftPenBackColor, rightPenForeColor, rightPenBackColor)
if ok:
    vs.Message('SetComponentPenColors succeeded')
else:
    vs.Message('SetComponentPenColors failed')
```

## See Also
VS Functions:
[GetComponentPenColors](GetComponentPenColors.md)

## Version
Availability: from VectorWorks 2008

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
