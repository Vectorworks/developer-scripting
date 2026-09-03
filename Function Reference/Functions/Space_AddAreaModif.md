# Space_AddAreaModif

## Description
Add Area Modifier to a space object.

```pascal
FUNCTION Space_AddAreaModif(
				space    : HANDLE;
				modifier : HANDLE) : BOOLEAN;
```

```python

def vs.Space_AddAreaModif(space, modifier):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE||
|modifier|HANDLE||

## Examples
```pascal
resultOK := Space_AddAreaModif(space, modifier);
```
```python
import vs

# Add Area Modifier to a space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer
modifier = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok = vs.Space_AddAreaModif(space, modifier)
if ok:
    vs.Message('Space_AddAreaModif succeeded')
else:
    vs.Message('Space_AddAreaModif failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
