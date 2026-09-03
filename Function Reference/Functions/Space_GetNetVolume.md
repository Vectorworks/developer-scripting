# Space_GetNetVolume

## Description
Returns net volume of given space object

```pascal
FUNCTION Space_GetNetVolume(space : HANDLE): REAL;
```

```python
def vs.Space_GetNetVolume(space):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |

## Examples
```pascal
resultVal := Space_GetNetVolume(space);
```
```python
import vs

# Returns net volume of given space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer

vol = vs.Space_GetNetVolume(space)
vs.Message('Space_GetNetVolume returned: ' + str(vol))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
