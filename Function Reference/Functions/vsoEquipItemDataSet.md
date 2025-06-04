# vsoEquipItemDataSet

## Description
Sets the specified equipment item data in the ParametricEquipmentItemDataMessage(92) message sent to a Script object based on the dataIndex.

```pascal
PROCEDURE vsoEquipItemDataSet(
				message   : LONGINT;
				dataIndex : INTEGER;
				dataValue : STRING);
```

```python
def vs.vsoEquipItemDataSet(message, dataIndex, dataValue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT|   |
|dataIndex|INTEGER|   |
|dataValue|STRING|   |

## Version
Availability: from Vectorworks 2023.4

## Category
* [Object Events](../Categories/Object%20Events.md)
