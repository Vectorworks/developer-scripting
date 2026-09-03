# GetComponentFillColors

## Description
Gets the fore and back fill colors of a component in an object.

```pascal
FUNCTION GetComponentFillColors(
				obj               : HANDLE;
				componentIndex    : INTEGER;
				VAR fillForeColor : INTEGER;
				VAR fillBackColor : INTEGER): BOOLEAN;
```

```python
def vs.GetComponentFillColors(obj, componentIndex):
    return (BOOLEAN, fillForeColor, fillBackColor)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|fillForeColor|INTEGER|Returns the fore color of the fill.|
|fillBackColor|INTEGER|Returns the back color of the fill.|

## Examples
```pascal
resultOK := GetComponentFillColors(obj, 1, 2, 3);
```
```python
import vs

# Gets the fore and back fill colors of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, fillForeColor, fillBackColor = vs.GetComponentFillColors(obj, componentIndex)
vs.Message('GetComponentFillColors returned: ' + str((ok, fillForeColor, fillBackColor)))
```

## See Also
VS Functions:
[SetComponentFillColors](SetComponentFillColors.md)

## Version
Availability: from VectorWorks 2008

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
