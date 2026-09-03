# LDevice_GetAccPos3D

## Description
Returns the 3D position and rotation of the specified accessory.

```pascal
PROCEDURE LDevice_GetAccPos3D(
				handle            : HANDLE;
				cellIndex         : LONGINT;
				accessoryIndex    : LONGINT;
				VAR outPosition3D : REAL;
				VAR outRotation3D : REAL);
```

```python
def vs.LDevice_GetAccPos3D(handle, cellIndex, accessoryIndex):
    return (outPosition3D, outRotation3D)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|cellIndex|LONGINT|   |
|accessoryIndex|LONGINT|   |
|outPosition3D|REAL|   |
|outRotation3D|REAL|   |

## Examples
```pascal
LDevice_GetAccPos3D(handle, 1, 2, 1.0, 2.0);
```
```python
import vs

# Returns the 3D position and rotation of the specified accessory.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
cellIndex = 1
accessoryIndex = 1

outPosition3D, outRotation3D = vs.LDevice_GetAccPos3D(handle, cellIndex, accessoryIndex)
vs.Message('LDevice_GetAccPos3D returned: ' + str((outPosition3D, outRotation3D)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
