# Space_CountAssignedZones

## Description
Returns count of assigned zones of the space object

```pascal
FUNCTION Space_CountAssignedZones(space : HANDLE): INTEGER;
```

```python
def vs.Space_CountAssignedZones(space):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |

## Examples
```pascal
resultN := Space_CountAssignedZones(space);
```
```python
import vs

# Returns count of assigned zones of the space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.Space_CountAssignedZones(space)
vs.Message('Space_CountAssignedZones returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
