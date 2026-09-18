# CollapseAllLBItems

## Description
This function is called when a list browser is in hierarchical display mode, and it removes all items that are not at the top level and closes all container items.

```pascal
PROCEDURE CollapseAllLBItems(
				dialogID    : LONGINT;
				componentID : LONGINT);
```

```python
def vs.CollapseAllLBItems(dialogID, componentID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog.|
|componentID|LONGINT|The id of the list browser.|

## Examples
```pascal
CollapseAllLBItems(1, 2);
```
```python
import vs

# This function is called when a list browser is in hierarchical display
# mode, and it removes all items that are not at the top level and closes all
# container.
dialogID = 1
componentID = 2

vs.CollapseAllLBItems(dialogID, componentID)
```

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
