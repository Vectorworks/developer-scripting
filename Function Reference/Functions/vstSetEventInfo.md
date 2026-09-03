# vstSetEventInfo

## Description
Sets the VS Tool Event Return Value

```pascal
PROCEDURE vstSetEventInfo(
				inAction     : LONGINT;
				inMessage1   : LONGINT;
				inMessage1   : LONGINT;
				inRsrcFileID : INTEGER);
```

```python
def vs.vstSetEventInfo(inAction, inMessage1, inMessage1, inRsrcFileID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inAction|LONGINT|   |
|inMessage1|LONGINT|   |
|inMessage1|LONGINT|   |
|inRsrcFileID|INTEGER|   |

## Examples
```pascal
vstSetEventInfo(1, 2, 3, 10);
```
```python
import vs

# Sets the VS Tool Event Return Value.
inAction = 1
inMessage1 = 2
inMessage1 = 3
inRsrcFileID = 10

vs.vstSetEventInfo(inAction, inMessage1, inMessage1, inRsrcFileID)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
