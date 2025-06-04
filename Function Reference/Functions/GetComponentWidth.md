# GetComponentWidth

## Description
Gets the width of a component in an object.

```pascal
FUNCTION GetComponentWidth(
				obj            : HANDLE;
				componentIndex : INTEGER;
				VAR width      : REAL): BOOLEAN;
```

```python
def vs.GetComponentWidth(obj, componentIndex):
    return (BOOLEAN, width)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|width|REAL|Returns the width of the component.|

## See Also
VS Functions:
[SetComponentWidth](SetComponentWidth.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
