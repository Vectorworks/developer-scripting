# Space_AddName

## Description
Add a new Space Name to the space object.

```pascal
PROCEDURE Space_AddName(
				space : HANDLE;
				name  : STRING);
```

```python
def vs.Space_AddName(space, name):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |
|name|STRING|   |

## Examples
```pascal
Space_AddName(space, 'Example');
```
```python
import vs

# Add a new Space Name to the space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer
name = 'Example'

vs.Space_AddName(space, name)
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
