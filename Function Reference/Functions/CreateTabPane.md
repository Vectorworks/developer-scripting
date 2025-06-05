# CreateTabPane

## Description
Creates a tab pane within a tab control on a dialog.

To define a tab pane, create a group control and add items to the group.  Arrange the items within the group.  Then call CreateTabPane to  add a new tab pane to a tab control.  Specify the group that defines the layout of that tab pane.

```pascal
PROCEDURE CreateTabPane(
				dialogID : LONGINT;
				itemID   : LONGINT;
				groupID  : LONGINT);
```

```python
def vs.CreateTabPane(dialogID, itemID, groupID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog.|
|itemID|LONGINT|The id of the Tab Control to which this tab pane will be added.|
|groupID|LONGINT|The id of the group that defines the tab pane.|

## Examples
[ComplexDialogLayout2](examples/ComplexDialogLayout2.md)

## See Also
VS Functions:
[CreateTabControl](CreateTabControl.md) 
| [CreateGroupBox](CreateGroupBox.md) 
| [RunLayoutDialog](RunLayoutDialog.md)

## Version
Availability: from VectorWorks10.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
