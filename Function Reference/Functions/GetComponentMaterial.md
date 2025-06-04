# GetComponentMaterial

## Description
Gets the material of a component in an object.

```pascal
FUNCTION GetComponentMaterial(
				object         : HANDLE;
				componentIndex : INTEGER;
				VAR material   : LONGINT): BOOLEAN;
```

```python
def vs.GetComponentMaterial(object, componentIndex):
    return (BOOLEAN, material)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|object|HANDLE|The object. Can be a wall, round wall, slab, roof face, roof, Wall Style, Slab Style, Roof Style, the Wall Preferences, the Slab Preferences, or the Roof Preferences.|
|componentIndex|INTEGER|The index of the component.|
|material|LONGINT|Returns the material of the component.|

## See Also
VS Functions:
[SetComponentMaterial](SetComponentMaterial.md)

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
