# GetComponentTexture

## Description
Gets the texture of a component in an object.

```pascal
FUNCTION GetComponentTexture(
				obj            : HANDLE;
				componentIndex : INTEGER;
				VAR texture    : LONGINT): BOOLEAN;
```

```python
def vs.GetComponentTexture(obj, componentIndex):
    return (BOOLEAN, texture)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, slab, Wall Style, Slab Style, the Wall Preferences, or the Slab Preferences.|
|componentIndex|INTEGER|The index of the component.|
|texture|LONGINT|Returns the ref number of the texture. 0 for no texture. -1 for class texture.|

## Examples
```pascal
resultOK := GetComponentTexture(obj, 1, 2);
```
```python
import vs

# Gets the texture of a component in an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
componentIndex = 1

ok, texture = vs.GetComponentTexture(obj, componentIndex)
vs.Message('GetComponentTexture returned: ' + str((ok, texture)))
```

## See Also
VS Functions:
[SetComponentTexture](SetComponentTexture.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
