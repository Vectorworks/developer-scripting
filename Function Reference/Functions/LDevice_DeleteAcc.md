# LDevice_DeleteAcc

## Description
Delete accessory attached to a Lighting Device.

```pascal
PROCEDURE LDevice_DeleteAcc(
				handle         : HANDLE;
				cellIndex      : LONGINT;
				accessoryIndex : LONGINT);
```

```python
def vs.LDevice_DeleteAcc(handle, cellIndex, accessoryIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|cellIndex|LONGINT|   |
|accessoryIndex|LONGINT|   |

## Examples
```pascal
LDevice_DeleteAcc(handle, 1, 2);
```
```python
import vs

# Delete accessory attached to a Lighting Device.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
cellIndex = 1
accessoryIndex = 1

vs.LDevice_DeleteAcc(handle, cellIndex, accessoryIndex)
```

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
