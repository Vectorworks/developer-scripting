# GetLineAttributeData

## Description
Get the current choices for the combined line style and line weight dialog control.  The line style value is an index and the line weight value is in mils.

```pascal
PROCEDURE GetLineAttributeData(
				dialogID       : LONGINT;
				itemID         : LONGINT;
				VAR lineStyle  : INTEGER;
				VAR lineWeight : INTEGER);
```

```python
def vs.GetLineAttributeData(dialogID, itemID):
    return (lineStyle, lineWeight)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |
|lineStyle|INTEGER|   |
|lineWeight|INTEGER|   |

## Examples
```pascal
GetLineAttributeData(1, 2, 3, 10);
```
```python
import vs

# Get the current choices for the combined line style and line weight dialog
# control.
dialogID = 1
itemID = 2

lineStyle, lineWeight = vs.GetLineAttributeData(dialogID, itemID)
vs.Message('GetLineAttributeData returned: ' + str((lineStyle, lineWeight)))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
