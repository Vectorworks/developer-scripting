# LDevice_AddAccessory

## Description
Add an accessory to a Lighting Device. Returns the index of the attached accessory.

```pascal
FUNCTION LDevice_AddAccessory(
				handle          : HANDLE;
				cellIndex       : LONGINT;
				accessorySymbol : HANDLE): LONGINT;
```

```python
def vs.LDevice_AddAccessory(handle, cellIndex, accessorySymbol):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|cellIndex|LONGINT|   |
|accessorySymbol|HANDLE|   |

## Examples
```pascal
resultN := LDevice_AddAccessory(handle, 1, accessorySymbol);
```
```python
import vs

# Add an accessory to a Lighting Device.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
cellIndex = 1
accessorySymbol = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

resultN = vs.LDevice_AddAccessory(handle, cellIndex, accessorySymbol)
vs.Message('LDevice_AddAccessory returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
