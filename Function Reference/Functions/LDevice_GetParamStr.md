# LDevice_GetParamStr

## Description
Get string parameter of a Lighting Device or attached Accessory by Worksheet Name. Use cell index 0 to operate on the first cell. Cell index -1 is not supported for Get.
Use accessory index -2 to ignore accessory values. Use accessory index 0 to operate on the first accessory of the specified cell. Accessory index -1 is not supported for Get.

```pascal
FUNCTION LDevice_GetParamStr(
				handle         : HANDLE;
				cellIndex      : LONGINT;
				accessoryIndex : LONGINT;
				universalName  : STRING): STRING;
```

```python
def vs.LDevice_GetParamStr(handle, cellIndex, accessoryIndex, universalName):
    return STRING
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
BEGIN
	lightingDeviceLabel := LDevice_GetParamStr(h, cellIndx, accIndx, 'Use Legend');
	IF (lightingDeviceLabel <> 'None') AND (NOT LabelExists(lightingDeviceLabel)) THEN
	BEGIN
		needsLabelReset := TRUE;
		counterInner 	:= accCountCell;

BEGIN
IF LDevice_GetParamStr(H,i,k,kIObType) = instType then outCount := outCount+1;
END
```
```python
import vs

# Get string parameter of a Lighting Device or attached Accessory by
# Worksheet Name.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
cellIndex = 1
accessoryIndex = 1
universalName = 'Example'

text = vs.LDevice_GetParamStr(handle, cellIndex, accessoryIndex, universalName)
vs.Message('LDevice_GetParamStr returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
