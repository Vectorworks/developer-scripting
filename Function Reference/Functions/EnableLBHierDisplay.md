# EnableLBHierDisplay

## Description
This function enables/disables the list browser to display items hierarchically. Calling this along will not change the display. The hierarchical display column must be set.

```pascal
PROCEDURE EnableLBHierDisplay(
				dialogID          : LONGINT;
				componentID       : LONGINT;
				enableHierDisplay : BOOLEAN);
```

```python
def vs.EnableLBHierDisplay(dialogID, componentID, enableHierDisplay):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog containing the list browser.|
|componentID|LONGINT|The id of the list browser.|
|enableHierDisplay|BOOLEAN|Whether to enable hierarchical display in the list browser.|

## See Also
VS Functions:
[SetLBHierDispColumn](SetLBHierDispColumn.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
