# vstResPDMenuInit

## Description
Use this call during tool setup. Initialize a tool resource popup created by vstAddResPDMenuMode and initialized by the ResList_* calls of the uniqueID identifying the resource list data.

```pascal
PROCEDURE vstResPDMenuInit(
				uniqueID  : STRING;
				modeGroup : INTEGER;
				emptyMsg  : STRING);
```

```python
def vs.vstResPDMenuInit(uniqueID, modeGroup, emptyMsg):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |
|modeGroup|INTEGER|   |
|emptyMsg|STRING|   |

## Examples
```pascal
vstResPDMenuInit('Example', 1, 'Example');
```
```python
import vs

# Use this call during tool setup.
uniqueID = 'Example'
modeGroup = 0
emptyMsg = 'Hello Vectorworks'

vs.vstResPDMenuInit(uniqueID, modeGroup, emptyMsg)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Tool Events](../Categories/Tool%20Events.md)
