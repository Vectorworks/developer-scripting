# RemoveListBoxTabStop

## Description
Removes the last tab stop from a Layout Manager list box.

```pascal
PROCEDURE RemoveListBoxTabStop(
				dialogID : LONGINT;
				itemID   : LONGINT);
```

```python
def vs.RemoveListBoxTabStop(dialogID, itemID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the dialog|
|itemID|LONGINT|ID of the list box|

## Examples
```pascal
RemoveListBoxTabStop(1, 2);
```
```python
import vs

# Removes the last tab stop from a Layout Manager list box.
dialogID = 1
itemID = 2

vs.RemoveListBoxTabStop(dialogID, itemID)
```

## See Also
VS Functions:
[AddListBoxTabStop](AddListBoxTabStop.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
