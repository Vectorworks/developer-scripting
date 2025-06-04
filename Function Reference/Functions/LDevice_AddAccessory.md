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

## Version
Availability: from Vectorworks 2021

## Category
* [Spotlight](../Categories/Spotlight.md)
