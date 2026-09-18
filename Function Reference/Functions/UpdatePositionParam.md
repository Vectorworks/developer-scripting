# UpdatePositionParam

## Description
Using the given position handle, changes the 'Position' parameter for all loads.

```pascal
PROCEDURE UpdatePositionParam(positionHandle : HANDLE);
```

```python
def vs.UpdatePositionParam(positionHandle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|positionHandle|HANDLE|   |

## Examples
```pascal
BEGIN
	UpdatePositionParam( parmHand );
END;
```
```python
import vs

# Using the given position handle, changes the 'Position' parameter for all
# loads.
positionHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.UpdatePositionParam(positionHandle)
```

## Version
Availability: from Vectorworks 2023

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
