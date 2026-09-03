# Space_GetGrossVolume

## Description
Returns gross volume of given space object

```pascal
FUNCTION Space_GetGrossVolume(space : HANDLE): REAL;
```

```python
def vs.Space_GetGrossVolume(space):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |

## Examples
```pascal
resultVal := Space_GetGrossVolume(space);
```
```python
import vs

# Returns gross volume of given space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer

vol = vs.Space_GetGrossVolume(space)
vs.Message('Space_GetGrossVolume returned: ' + str(vol))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
