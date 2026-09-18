# LDevice_SetAccPos3D

## Description
Set the 3D position and rotation of the specified accessory.

```pascal
PROCEDURE LDevice_SetAccPos3D(
				handle         : HANDLE;
				cellIndex      : LONGINT;
				accessoryIndex : LONGINT;
				position3D     : REAL;
				rotation3D     : REAL);
```

```python
def vs.LDevice_SetAccPos3D(handle, cellIndex, accessoryIndex, position3D, rotation3D):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|cellIndex|LONGINT|   |
|accessoryIndex|LONGINT|   |
|position3D|REAL|   |
|rotation3D|REAL|   |

## Examples
```pascal
LDevice_SetAccPos3D(handle, 1, 2, 1.0, 2.0);
```
```python
import vs

# Set the 3D position and rotation of the specified accessory.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
cellIndex = 1
accessoryIndex = 1
position3D = 1.0
rotation3D = 2.0

vs.LDevice_SetAccPos3D(handle, cellIndex, accessoryIndex, position3D, rotation3D)
```

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
