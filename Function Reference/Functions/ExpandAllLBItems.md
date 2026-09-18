# ExpandAllLBItems

## Description
This function is called when a list browser is in hierarchical display mode, and it redisplays all items that were hidden and opens all the containers.

```pascal
PROCEDURE ExpandAllLBItems(
				dialogID    : LONGINT;
				componentID : LONGINT);
```

```python
def vs.ExpandAllLBItems(dialogID, componentID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog.|
|componentID|LONGINT|The id of the list browser.|

## Examples
```pascal
ExpandAllLBItems(1, 2);
```
```python
import vs

# This function is called when a list browser is in hierarchical display
# mode, and it redisplays all items that were hidden and opens all the
# containers.
dialogID = 1
componentID = 2

vs.ExpandAllLBItems(dialogID, componentID)
```

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
