# LDevice_GetParamLong

## Description
Get long integer parameter of a Lighting Device or attached Accessory by Worksheet Name. Use cell index 0 to operate on the first cell. Cell index -1 is not supported for Get.
Use accessory index -2 to ignore accessory values. Use accessory index 0 to operate on the first accessory of the specified cell. Accessory index -1 is not supported for Get.

```pascal
FUNCTION LDevice_GetParamLong(
				handle         : HANDLE;
				cellIndex      : LONGINT;
				accessoryIndex : LONGINT;
				universalName  : STRING): LONGINT;
```

```python
def vs.LDevice_GetParamLong(handle, cellIndex, accessoryIndex, universalName):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|cellIndex|LONGINT|   |
|accessoryIndex|LONGINT|   |
|universalName|STRING|   |

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
