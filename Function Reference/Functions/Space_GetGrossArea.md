# Space_GetGrossArea

## Description
Returns gross area of given space object

```pascal
FUNCTION Space_GetGrossArea(space : HANDLE): REAL;
```

```python
def vs.Space_GetGrossArea(space):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |

## Examples
```pascal
resultVal := Space_GetGrossArea(space);
```
```python
import vs

# Returns gross area of given space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer

area = vs.Space_GetGrossArea(space)
vs.Message('Space_GetGrossArea returned: ' + str(area))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
