# LDevice_SetParamReal

## Description
Set real parameter of a Lighting Device or attached Accessory by Worksheet Name. Use cell index 0 to operate on the first cell. Use cell index -1 to set value for all the cells.
Use accessory index -2 to ignore accessory values. Use accessory index 0 to operate on the first accessory of the specified cell. Use accessory index -1 to set value for all the accessories on the specified cell.

```pascal
PROCEDURE LDevice_SetParamReal(
				handle         : HANDLE;
				cellIndex      : LONGINT;
				accessoryIndex : LONGINT;
				universalName  : STRING;
				newValue       : REAL);
```

```python
def vs.LDevice_SetParamReal(handle, cellIndex, accessoryIndex, universalName, newValue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|cellIndex|LONGINT|   |
|accessoryIndex|LONGINT|   |
|universalName|STRING|   |
|newValue|REAL|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
