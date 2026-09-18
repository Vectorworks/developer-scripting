# LDevice_SetAccPos2D

## Description
Set the 2D position and rotation of the specified accessory.

```pascal
PROCEDURE LDevice_SetAccPos2D(
				handle         : HANDLE;
				cellIndex      : LONGINT;
				accessoryIndex : LONGINT;
				position       : REAL;
				rotation       : REAL);
```

```python
def vs.LDevice_SetAccPos2D(handle, cellIndex, accessoryIndex, position, rotation):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|cellIndex|LONGINT|   |
|accessoryIndex|LONGINT|   |
|position|REAL|   |
|rotation|REAL|   |

## Examples
```pascal
LDevice_SetAccPos2D(handle, 1, 2, 1.0, 2.0);
```
```python
import vs

# Set the 2D position and rotation of the specified accessory.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
cellIndex = 1
accessoryIndex = 1
position = 1.0
rotation = 2.0

vs.LDevice_SetAccPos2D(handle, cellIndex, accessoryIndex, position, rotation)
```

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
