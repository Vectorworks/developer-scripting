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

## See Also
VS Functions:
[GetCoreWallComponent](GetCoreWallComponent.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
