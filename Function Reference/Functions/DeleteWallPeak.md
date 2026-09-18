# DeleteWallPeak

## Description
Deletes the wall peak at the given index number

```pascal
PROCEDURE DeleteWallPeak(
				wallHandle : HANDLE;
				index      : INTEGER);
```

```python
def vs.DeleteWallPeak(wallHandle, index):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wallHandle|HANDLE|   |
|index|INTEGER|   |

## Examples
```pascal
DeleteWallPeak(wallHandle, 1);
```
```python
import vs

# Deletes the wall peak at the given index number.
wallHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
index = 1

vs.DeleteWallPeak(wallHandle, index)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
