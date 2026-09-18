# Space_DeassignZone

## Description
Deassign Zone from a space object.

```pascal
PROCEDURE Space_DeassignZone(
				space    : HANDLE;
				zoneType : STRING;
				zoneName : STRING);
```

```python
def vs.Space_DeassignZone(space, zoneType, zoneName):
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
Space_DeassignZone(space, 'Example', 'Example');
```
```python
import vs

# Deassign Zone from a space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer
zoneType = 'Example'
zoneName = 'Example'

vs.Space_DeassignZone(space, zoneType, zoneName)
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
