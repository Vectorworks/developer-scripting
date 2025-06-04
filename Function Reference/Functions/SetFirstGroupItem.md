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
[DWD 1/20/00]

## Examples
alogLayoutPulldownMenu}}
{{ComplexDialogLayout2}}

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
