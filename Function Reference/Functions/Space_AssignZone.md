# Space_AssignZone

## Description
Assign Zone to the space object.

```pascal
PROCEDURE Space_AssignZone(
				space    : HANDLE;
				zoneType : STRING;
				zoneName : STRING);
```

```python
def vs.Space_AssignZone(space, zoneType, zoneName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |
|zoneType|STRING|   |
|zoneName|STRING|   |

## Examples
```pascal
Space_AssignZone(space, 'Example', 'Example');
```
```python
import vs

# Assign Zone to the space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer
zoneType = 'Example'
zoneName = 'Example'

vs.Space_AssignZone(space, zoneType, zoneName)
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
