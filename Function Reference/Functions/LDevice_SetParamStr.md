# LDevice_SetParamStr

## Description
Set string parameter of a Lighting Device or attached Accessory by Worksheet Name. Use cell index 0 to operate on the first cell. Use cell index -1 to set value for all the cells.
Use accessory index -2 to ignore accessory values. Use accessory index 0 to operate on the first accessory of the specified cell. Use accessory index -1 to set value for all the accessories on the specified cell.

```pascal
PROCEDURE LDevice_SetParamStr(
				handle         : HANDLE;
				cellIndex      : LONGINT;
				accessoryIndex : LONGINT;
				universalName  : STRING;
				newValue       : STRING);
```

```python
def vs.LDevice_SetParamStr(handle, cellIndex, accessoryIndex, universalName, newValue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|cellIndex|LONGINT|   |
|accessoryIndex|LONGINT|   |
|universalName|STRING|   |
|newValue|STRING|   |

## Examples
```pascal
LDevice_SetParamStr(handle, 1, 2, 'Example', 'Example');
```
```python
import vs

# Set string parameter of a Lighting Device or attached Accessory by
# Worksheet Name.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
cellIndex = 1
accessoryIndex = 1
universalName = 'Example'
newValue = 'Example'

vs.LDevice_SetParamStr(handle, cellIndex, accessoryIndex, universalName, newValue)
```

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
