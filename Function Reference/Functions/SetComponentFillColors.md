# SetComponentFillColors

## Description
Sets the fore and back fill colors of a component in an object.

```pascal
FUNCTION SetComponentFillColors(
				obj            : HANDLE;
				componentIndex : INTEGER;
				fillForeColor  : INTEGER;
				fillBackColor  : INTEGER): BOOLEAN;
```

```python
def vs.SetComponentFillColors(obj, componentIndex, fillForeColor, fillBackColor):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|fillForeColor|INTEGER|The fore color of the fill.|
|fillBackColor|INTEGER|The back color of the fill.|

## Examples
```pascal
resultOK := SetComponentFillColors(obj, 1, 2, 3);
```
```python
import vs

# Sets the fore and back fill colors of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
fillForeColor = 5
fillBackColor = 5

ok = vs.SetComponentFillColors(obj, componentIndex, fillForeColor, fillBackColor)
if ok:
    vs.Message('SetComponentFillColors succeeded')
else:
    vs.Message('SetComponentFillColors failed')
```

## See Also
VS Functions:
[GetComponentFillColors](GetComponentFillColors.md)

## Version
Availability: from VectorWorks 2008

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
