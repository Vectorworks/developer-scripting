# Space_CountAssZones

## Description
Returns count of assigned zones of the space object

```pascal
FUNCTION Space_CountAssZones(space : HANDLE) : INTEGER;
```

```python

def vs.Space_CountAssZones(space):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE||

## Examples
```pascal
resultN := Space_CountAssZones(space);
```
```python
import vs

# Returns count of assigned zones of the space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.Space_CountAssZones(space)
vs.Message('Space_CountAssZones returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
