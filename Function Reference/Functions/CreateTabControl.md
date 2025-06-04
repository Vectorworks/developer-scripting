# CreateTabControl

## Description
Creates a tab control within a dialog.  The tab control manages the display of multiple panes of information and provides tab buttons that allow the user to swtich between panes. 

To create a tab control in a dialog, first define a group for each tab pane.  Add other controls to the groups and arrange them.  Then call CreateTabControl with an id.  Finally, call CreateTabPane for each pane providing the id of the group that defines that pane.

```pascal
PROCEDURE CreateTabControl(
				dialogID : LONGINT;
				itemID   : LONGINT);
```

```python
def vs.CreateTabControl(dialogID, itemID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The id of the dialog that contains this Tab control.|
|itemID|LONGINT|The id of the Tab control.|

## Examples
mplexDialogLayout2}}

## See Also
VS Functions:
[CreateTabPane](CreateTabPane.md) 
| [CreateGroupBox](CreateGroupBox.md) 
| [RunLayoutDialog](RunLayoutDialog.md)

## Version
Availability: from VectorWorks10.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
