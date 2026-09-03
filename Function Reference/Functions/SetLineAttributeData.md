# SetLineAttributeData

## Description
Set current choices for the line attribute dialog control.  Both the line style index and the line weight in mils can be specified.

```pascal
PROCEDURE SetLineAttributeData(
				dialogID   : LONGINT;
				itemID     : LONGINT;
				lineStyle  : INTEGER;
				lineWeight : INTEGER);
```

```python
def vs.SetLineAttributeData(dialogID, itemID, lineStyle, lineWeight):
    return None
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
SetLineAttributeData(1, 2, 3, 10);
```
```python
import vs

# Set current choices for the line attribute dialog control.
dialogID = 1
itemID = 2
lineStyle = 0
lineWeight = 3

vs.SetLineAttributeData(dialogID, itemID, lineStyle, lineWeight)
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
