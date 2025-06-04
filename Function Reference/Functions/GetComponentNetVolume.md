# GetComponentNetVolume

## Description
Gets the net volume of a component in an object.

```pascal
FUNCTION GetComponentNetVolume(
				obj            : HANDLE;
				componentIndex : INTEGER): REAL;
```

```python
def vs.GetComponentNetVolume(obj, componentIndex):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|

## See Also
VS Functions:
[GetComponentNetArea](GetComponentNetArea.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
