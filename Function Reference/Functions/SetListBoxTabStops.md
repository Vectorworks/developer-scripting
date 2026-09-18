# SetListBoxTabStops

## Description
Set tab stops for list control.

```pascal
PROCEDURE SetListBoxTabStops(
				dialogID    : LONGINT;
				componentID : LONGINT;
				tabStops    : ARRAY);
```

```python
def vs.SetListBoxTabStops(dialogID, componentID, tabStops):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|tabStops|ARRAY|   |

## Examples
```pascal
SetListBoxTabStops(1, 2, tabStops);
```
```python
import vs

# Set tab stops for list control.
dialogID = 1
componentID = 2
tabStops = []

vs.SetListBoxTabStops(dialogID, componentID, tabStops)
```

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
