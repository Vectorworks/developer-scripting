# Space_ItemAvZones

## Description
Returns available zone (item) of space tool

```pascal
FUNCTION Space_ItemAvZones(item : INTEGER) : STRING;
```

```python

def vs.Space_ItemAvZones(item):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|item|INTEGER||

## Examples
```pascal
resultStr := Space_ItemAvZones(1);
```
```python
import vs

# Returns available zone (item) of space tool.
item = 1

text = vs.Space_ItemAvZones(item)
vs.Message('Space_ItemAvZones returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
