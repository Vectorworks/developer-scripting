# SetComponentMaterial

## Description
Sets the material of a component in an object.

```pascal
FUNCTION SetComponentMaterial(
				object         : HANDLE;
				componentIndex : INTEGER;
				material       : LONGINT): BOOLEAN;
```

```python
def vs.SetComponentMaterial(object, componentIndex, material):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|material|LONGINT|The material of the component.|

## See Also
VS Functions:
[GetComponentMaterial](GetComponentMaterial.md)

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
