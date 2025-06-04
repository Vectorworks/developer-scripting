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

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
