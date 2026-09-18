# LDevice_GetAccPos2D

## Description
Returns the 2D position and rotation of the specified accessory.

```pascal
PROCEDURE LDevice_GetAccPos2D(
				handle          : HANDLE;
				cellIndex       : LONGINT;
				accessoryIndex  : LONGINT;
				VAR outPosition : REAL;
				VAR outRotation : REAL);
```

```python
def vs.LDevice_GetAccPos2D(handle, cellIndex, accessoryIndex):
    return (outPosition, outRotation)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|cellIndex|LONGINT|   |
|accessoryIndex|LONGINT|   |
|outPosition|REAL|   |
|outRotation|REAL|   |

## Examples
```pascal
LDevice_GetAccPos2D(handle, 1, 2, 1.0, 2.0);
```
```python
import vs

# Returns the 2D position and rotation of the specified accessory.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
cellIndex = 1
accessoryIndex = 1

outPosition, outRotation = vs.LDevice_GetAccPos2D(handle, cellIndex, accessoryIndex)
vs.Message('LDevice_GetAccPos2D returned: ' + str((outPosition, outRotation)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
