# SetComponentWidth

## Description
Sets the width of a component in an object.

```pascal
FUNCTION SetComponentWidth(
				obj            : HANDLE;
				componentIndex : INTEGER;
				width          : REAL): BOOLEAN;
```

```python
def vs.SetComponentWidth(obj, componentIndex, width):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|width|REAL|The width of the component.|

## See Also
VS Functions:
[GetComponentWidth](GetComponentWidth.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
