# Space_ItemAssignedZones

## Description
Returns assigned zone (item) of space object

```pascal
FUNCTION Space_ItemAssignedZones(
				space : HANDLE;
				item  : INTEGER): STRING;
```

```python
def vs.Space_ItemAssignedZones(space, item):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |
|item|INTEGER|   |

## Examples
```pascal
resultStr := Space_ItemAssignedZones(space, 1);
```
```python
import vs

# Returns assigned zone (item) of space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer
item = 1

text = vs.Space_ItemAssignedZones(space, item)
vs.Message('Space_ItemAssignedZones returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
