# LDevice_GetParamBool

## Description
Get boolean parameter of a Lighting Device or attached Accessory by Worksheet Name. Use cell index 0 to operate on the first cell. Cell index -1 is not supported for Get.
Use accessory index -2 to ignore accessory values. Use accessory index 0 to operate on the first accessory of the specified cell. Accessory index -1 is not supported for Get.

```pascal
FUNCTION LDevice_GetParamBool(
				handle         : HANDLE;
				cellIndex      : LONGINT;
				accessoryIndex : LONGINT;
				universalName  : STRING): BOOLEAN;
```

```python
def vs.LDevice_GetParamBool(handle, cellIndex, accessoryIndex, universalName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|cellIndex|LONGINT|   |
|accessoryIndex|LONGINT|   |
|universalName|STRING|   |

## Examples
```pascal
resultOK := LDevice_GetParamBool(handle, 1, 2, 'Example');
```
```python
import vs

# Get boolean parameter of a Lighting Device or attached Accessory by
# Worksheet Name.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
cellIndex = 1
accessoryIndex = 1
universalName = 'Example'

ok = vs.LDevice_GetParamBool(handle, cellIndex, accessoryIndex, universalName)
if ok:
    vs.Message('LDevice_GetParamBool succeeded')
else:
    vs.Message('LDevice_GetParamBool failed')
```

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
