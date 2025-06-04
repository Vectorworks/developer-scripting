# LDevice_GetParamReal

## Description
Get real parameter of a Lighting Device or attached Accessory by Worksheet Name. Use cell index 0 to operate on the first cell. Cell index -1 is not supported for Get.
Use accessory index -2 to ignore accessory values. Use accessory index 0 to operate on the first accessory of the specified cell. Accessory index -1 is not supported for Get.

```pascal
FUNCTION LDevice_GetParamReal(
				handle         : HANDLE;
				cellIndex      : LONGINT;
				accessoryIndex : LONGINT;
				universalName  : STRING): REAL;
```

```python
def vs.LDevice_GetParamReal(handle, cellIndex, accessoryIndex, universalName):
    return REAL
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
