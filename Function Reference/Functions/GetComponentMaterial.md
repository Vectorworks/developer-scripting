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

## Examples
```pascal
resultOK := GetComponentMaterial(object, 1, 2);
```
```python
import vs

# Gets the material of a component in an object.
object = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, material = vs.GetComponentMaterial(object, componentIndex)
vs.Message('GetComponentMaterial returned: ' + str((ok, material)))
```

## See Also
VS Functions:
[SetComponentMaterial](SetComponentMaterial.md)

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
