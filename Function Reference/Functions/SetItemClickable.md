# SetItemClickable

## Description
Sets the specified item to generate events when clicked.  Currently only static text and images are supported.
Remark: Use in the dialogs setup event handler. Changes the cursor if the mouse is over the item to indicate its clickability.

```pascal
PROCEDURE SetItemClickable(
				dialogID    : LONGINT;
				componentID : LONGINT;
				clickable   : BOOLEAN);
```

```python
def vs.SetItemClickable(dialogID, componentID, clickable):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|clickable|BOOLEAN|   |

## Examples
```pascal
SetItemClickable(1, 2, TRUE);
```
```python
import vs

# Sets the specified item to generate events when clicked.
dialogID = 1
componentID = 2
clickable = True

vs.SetItemClickable(dialogID, componentID, clickable)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
