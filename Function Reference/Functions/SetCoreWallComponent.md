# SetCoreWallComponent

## Description
Sets the core wall component of an object.

```pascal
PROCEDURE SetCoreWallComponent(
				obj               : HANDLE;
				coreWallComponent : INTEGER);
```

```python
def vs.SetCoreWallComponent(obj, coreWallComponent):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object. Can be a wall, round wall, Wall Style, or the Wall Preferences.|
|coreWallComponent|INTEGER|The index of the core wall component.  0 will cause there to be no core wall component.|

## Examples
```pascal
SetCoreWallComponent(obj, 1);
```
```python
import vs

# Sets the core wall component of an object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
coreWallComponent = 1

vs.SetCoreWallComponent(obj, coreWallComponent)
```

## See Also
VS Functions:
[GetCoreWallComponent](GetCoreWallComponent.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
