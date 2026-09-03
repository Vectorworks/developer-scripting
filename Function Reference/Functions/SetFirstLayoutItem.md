# SetFirstLayoutItem

## Description
Initializes dialog control layout by placing the specified control item in the top left corner of the layout. All other controls in the layout are positioned relative to the control item placed with this function.

```pascal
PROCEDURE SetFirstLayoutItem(
				dialogID    : LONGINT;
				firstItemID : LONGINT);
```

```python
def vs.SetFirstLayoutItem(dialogID, firstItemID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout being defined.|
|firstItemID|LONGINT|The index of the control item to be placed.|

## Remarks
[DWD 1/20/00]

## Examples
* [DialogLayoutPulldownMenu](examples/DialogLayoutPulldownMenu.md)
* [ComplexDialogLayout2](examples/ComplexDialogLayout2.md)

```pascal
{* Position dialog control items *}
SetFirstLayoutItem (dialogID, 3);
SetRightItem (dialogID, 3, 4, 0, 0);
SetBelowItem (dialogID, 3, 5, 0, 0);
SetRightItem (dialogID, 5, 6, 0, 0);
SetBelowItem (dialogID, 5, 7, 0, 0);

{* Position dialog control items *}
	SetFirstLayoutItem (dialogID, 3);
	SetFirstGroupItem (dialogID, 3, 4);
	SetBelowItem (dialogID, 4, 5, 0, 2);
	SetRightItem (dialogID, 4, 6, 0, 0);
	SetRightItem (dialogID, 5, 7, 0, 0);

{* Position the control items *}
	SetFirstLayoutItem (dialogID, 4);
	SetBelowItem (dialogID, 4, 5, 0, 4);
	SetBelowItem (dialogID, 5, 7, 0, 1);
```
```python
import vs

# Initializes dialog control layout by placing the specified control item in
# the top left corner of the layout.
dialogID = 1
firstItemID = 2

vs.SetFirstLayoutItem(dialogID, firstItemID)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
