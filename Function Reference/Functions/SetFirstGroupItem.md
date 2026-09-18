# SetFirstGroupItem

## Description
Places the first item of a layout group into the specified group box control item. The control is inserted in the top left corner of the group box, and all other controls in the group are placed relative to this item.

```pascal
PROCEDURE SetFirstGroupItem(
				dialogID    : LONGINT;
				groupID     : LONGINT;
				firstItemID : LONGINT);
```

```python
def vs.SetFirstGroupItem(dialogID, groupID, firstItemID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout being defined.|
|groupID|LONGINT|The index of the group box control accepting the first item.|
|firstItemID|LONGINT|The index of the control item to be placed in the group box.|

## Remarks

## Examples
* [DialogLayoutPulldownMenu](examples/DialogLayoutPulldownMenu.md)
* [ComplexDialogLayout2](examples/ComplexDialogLayout2.md)

```pascal
{* Position dialog control items *}
	SetFirstLayoutItem (dialogID, 3);
	SetFirstGroupItem (dialogID, 3, 4);
	SetBelowItem (dialogID, 4, 5, 0, 2);
	SetRightItem (dialogID, 4, 6, 0, 0);
	SetRightItem (dialogID, 5, 7, 0, 0);

{* Position the control items *}
	SetFirstLayoutItem (dialogID, 199);
	SetFirstGroupItem (dialogID, 199, 7);
	FOR i := 1 TO gNumFieldsD - 1 DO
		SetBelowItem (dialogID, 2*i+5, 2*i+7, 0, 1);

{* Wire controls into swap panes *}
	CreateSwapPane (dialogID, 12, 15);
	SetFirstGroupItem(dialogID, 15, 13);
	CreateSwapPane (dialogID, 12, 16);
	SetFirstGroupItem(dialogID, 16, 14);
```
```python
import vs

# Places the first item of a layout group into the specified group box
# control item.
dialogID = 1
groupID = 2
firstItemID = 3

vs.SetFirstGroupItem(dialogID, groupID, firstItemID)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
