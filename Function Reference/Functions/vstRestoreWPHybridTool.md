# vstRestoreWPHybridTool

## Description
Restore the working plane after hybrid tool [vstSetWPHybridTool](vstSetWPHybridTool.md).

```pascal
PROCEDURE vstRestoreWPHybridTool(message1 : LONGINT);
```

```python
def vs.vstRestoreWPHybridTool(message1):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message1|LONGINT|   |

## Examples
```pascal
vstRestoreWPHybridTool(1);
```
```python
import vs

# Restore the working plane after hybrid tool vstSetWPHybridTool.
message1 = 1

vs.vstRestoreWPHybridTool(message1)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Tool Events](../Categories/Tool%20Events.md)
