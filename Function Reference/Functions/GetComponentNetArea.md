# GetComponentNetArea

## Description
Gets the net area of a component in an object.

```pascal
FUNCTION GetComponentNetArea(
				obj            : HANDLE;
				componentIndex : INTEGER): REAL;
```

```python
def vs.GetComponentNetArea(obj, componentIndex):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|

## See Also
VS Functions:
[GetComponentNetVolume](GetComponentNetVolume.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
