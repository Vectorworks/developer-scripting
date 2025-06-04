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

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
