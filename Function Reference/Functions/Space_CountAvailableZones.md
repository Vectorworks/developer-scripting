# Space_CountAvailableZones

## Description
Returns count of available zones of the space tool

```pascal
FUNCTION Space_CountAvailableZones : INTEGER;
```

```python
def vs.Space_CountAvailableZones():
    return INTEGER
```

## Examples
```pascal
resultN := Space_CountAvailableZones;
```
```python
import vs

# Returns count of available zones of the space tool.
count = vs.Space_CountAvailableZones()
vs.Message('Space_CountAvailableZones returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
