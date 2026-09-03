# vstSetWPHybridTool

## Description
Set the working plane on the layer preparing it for hybrid tool.

```pascal
PROCEDURE vstSetWPHybridTool(message1 : LONGINT);
```

```python
def vs.vstSetWPHybridTool(message1):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message1|LONGINT|   |

## Examples
```pascal
vstSetWPHybridTool( modeGroup );
vstSetCursorByView;
```
```python
import vs

# Set the working plane on the layer preparing it for hybrid tool.
message1 = 1

vs.vstSetWPHybridTool(message1)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Tool Events](../Categories/Tool%20Events.md)
