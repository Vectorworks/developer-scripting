# Space_AddAreaModifierToSpace

## Description
Add Area Modifier to a space object.

```pascal
PROCEDURE Space_AddAreaModifierToSpace(
				space    : HANDLE;
				modifier : STRING);
```

```python
def vs.Space_AddAreaModifierToSpace(space, modifier):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |
|modifier|STRING|   |

## Examples
```pascal
Space_AddAreaModifierToSpace(space, 'Example');
```
```python
import vs

# Add Area Modifier to a space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer
modifier = 'Example'

vs.Space_AddAreaModifierToSpace(space, modifier)
```

## Version
Availability: from Vectorworks 2014 - renamed [[VS:Space_AddAreaModif]] with Vectorworks 2024.

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
