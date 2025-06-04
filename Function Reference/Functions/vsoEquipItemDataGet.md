# vsoEquipItemDataGet

## Description
Gets the specified equipment item data from the ParametricEquipmentItemDataMessage(92) message sent to a Script object based on the dataIndex. Returns false if this value is not available.

```pascal
FUNCTION vsoEquipItemDataGet(
				message      : LONGINT;
				dataIndex    : INTEGER;
				VAR outValue : STRING): BOOLEAN;
```

```python
def vs.vsoEquipItemDataGet(message, dataIndex):
    return (BOOLEAN, outValue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT|   |
|dataIndex|INTEGER|   |
|outValue|STRING|   |

## Version
Availability: from Vectorworks 2023.4

## Category
* [Object Events](../Categories/Object%20Events.md)
