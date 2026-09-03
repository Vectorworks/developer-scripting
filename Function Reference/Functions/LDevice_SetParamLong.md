# LDevice_SetParamLong

## Description
Set long integer parameter of a Lighting Device or attached Accessory by Worksheet Name. Use cell index 0 to operate on the first cell. Use cell index -1 to set value for all the cells.
Use accessory index -2 to ignore accessory values. Use accessory index 0 to operate on the first accessory of the specified cell. Use accessory index -1 to set value for all the accessories on the specified cell.

```pascal
PROCEDURE LDevice_SetParamLong(
				handle         : HANDLE;
				cellIndex      : LONGINT;
				accessoryIndex : LONGINT;
				universalName  : STRING;
				newValue       : LONGINT);
```

```python
def vs.LDevice_SetParamLong(handle, cellIndex, accessoryIndex, universalName, newValue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|cellIndex|LONGINT|   |
|accessoryIndex|LONGINT|   |
|universalName|STRING|   |
|newValue|LONGINT|   |

## Examples
```pascal
LDevice_SetParamLong(handle, 1, 2, 'Example', 3);
```
```python
import vs

# Set long integer parameter of a Lighting Device or attached Accessory by
# Worksheet Name.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
cellIndex = 1
accessoryIndex = 1
universalName = 'Example'
newValue = 1

vs.LDevice_SetParamLong(handle, cellIndex, accessoryIndex, universalName, newValue)
```

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
