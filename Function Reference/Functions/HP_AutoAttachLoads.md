# HP_AutoAttachLoads

## Description
Using the given position handle, attaches all loads, that can be calculated as a part of the system and loads attached to the geometry in the position.

```pascal
PROCEDURE HP_AutoAttachLoads(positionHandle : HANDLE);
```

```python
def vs.HP_AutoAttachLoads(positionHandle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|positionHandle|HANDLE|   |

## Examples
```pascal
BEGIN
	SetSelect(ConvertedObjects[I]);
	HP_AutoAttachLoads(ConvertedObjects[I]);
END;
```
```python
import vs

# Using the given position handle, attaches all loads, that can be calculated
# as a part of the system and loads attached to the geometry in the position.
positionHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.HP_AutoAttachLoads(positionHandle)
```

## Version
Availability: from Vectorworks 2019

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
