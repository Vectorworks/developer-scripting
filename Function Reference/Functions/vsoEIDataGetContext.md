# vsoEIDataGetContext

## Description
Gets the equipment item data context from the ParametricEquipmentItemDataMessage(92) message sent to a Script object.

```pascal
FUNCTION vsoEIDataGetContext(message : LONGINT): INTEGER;
```

```python
def vs.vsoEIDataGetContext(message):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|LONGINT|   |

## Examples
```pascal
resultN := vsoEIDataGetContext(1);
```
```python
import vs

# Gets the equipment item data context from the
# ParametricEquipmentItemDataMessage(92) message sent to a Script object.
message = 'Hello Vectorworks'

resultN = vs.vsoEIDataGetContext(message)
vs.Message('vsoEIDataGetContext returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [Object Events](../Categories/Object%20Events.md)
