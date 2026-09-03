# SetComponentFill

## Description
Sets the fill of a component in an object.

```pascal
FUNCTION SetComponentFill(
				obj            : HANDLE;
				componentIndex : INTEGER;
				fill           : LONGINT): BOOLEAN;
```

```python
def vs.SetComponentFill(obj, componentIndex, fill):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|fill|LONGINT|The fill of the component.  Positive values for patterns, negative object indexes for hatches.|

## Examples
```pascal
resultOK := SetComponentFill(obj, 1, 2);
```
```python
import vs

# Sets the fill of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1
fill = 1

ok = vs.SetComponentFill(obj, componentIndex, fill)
if ok:
    vs.Message('SetComponentFill succeeded')
else:
    vs.Message('SetComponentFill failed')
```

## See Also
VS Functions:
[GetComponentFill](GetComponentFill.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
