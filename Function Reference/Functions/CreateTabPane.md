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

```pascal
{ project pane }
CreateTabPane     (dialog1,  4,   5);
SetFirstGroupItem (dialog1,  5,   6);
SetRightItem      (dialog1,  6,   7,  0, 0);
SetBelowItem      (dialog1,  6,   8,  0, 4);
SetRightItem      (dialog1,  8,   9,  0, 0);

BEGIN
	CreateTabPane (dialogID, 4, fieldNum);
	SetFirstGroupItem (dialogID, fieldNum, gbIDNum);
END

{General Tab}
CreateTabPane     (dialog1, kTabControl,            kGenTab);
SetFirstGroupItem (dialog1, kGenTab,                kGeneralImage);
SetRightItem      (dialog1, kGeneralImage,          kGenHidGroup,           0, -1);
SetFirstGroupItem (dialog1, kGenHidGroup,           kOverallHgtGrp);
SetFirstGroupItem (dialog1, kOverallHgtGrp,         kHeightByLayer);
```
```python
import vs

# Creates a tab pane within a tab control on a dialog.
dialogID = 1
itemID = 2
groupID = 3

vs.CreateTabPane(dialogID, itemID, groupID)
newObj = vs.LNewObj()  # handle to the newly created object
```

## See Also
VS Functions:
[CreateTabControl](CreateTabControl.md) 
| [CreateGroupBox](CreateGroupBox.md) 
| [RunLayoutDialog](RunLayoutDialog.md)

## Version
Availability: from VectorWorks10.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
