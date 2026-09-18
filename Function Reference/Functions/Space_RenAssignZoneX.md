# Space_RenAssignZoneX

## Description
Rename existing Zone (x) from a space object.

```pascal
PROCEDURE Space_RenAssignZoneX(
				space    : HANDLE;
				index    : INTEGER;
				zoneType : STRING;
				zoneName : STRING);
```

```python

def vs.Space_RenAssignZoneX(space, index, zoneType, zoneName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE||
|index|INTEGER||
|zoneType|STRING||
|zoneName|STRING||

## Examples
```pascal
Space_RenAssignZoneX(space, 1, 'Example', 'Example');
```
```python
import vs

# Rename existing Zone (x) from a space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1
zoneType = 'Example'
zoneName = 'Example'

vs.Space_RenAssignZoneX(space, index, zoneType, zoneName)
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
