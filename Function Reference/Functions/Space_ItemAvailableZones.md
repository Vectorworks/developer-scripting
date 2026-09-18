# Space_ItemAvailableZones

## Description
Returns available zone (item) of space tool

```pascal
FUNCTION Space_ItemAvailableZones(item : INTEGER): STRING;
```

```python
def vs.Space_ItemAvailableZones(item):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|item|INTEGER|   |

## Examples
```pascal
resultStr := Space_ItemAvailableZones(1);
```
```python
import vs

# Returns available zone (item) of space tool.
item = 1

text = vs.Space_ItemAvailableZones(item)
vs.Message('Space_ItemAvailableZones returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
