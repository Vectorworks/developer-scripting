# CreateResourcePopup

## Description
Creates a text popup similar to a pulldown menu that opens a Resource Manager window.<BR>
<BR>
This is basically the same as the Thumbnail popup but the control only displays the name of the selected item (it does not display its thumbnail), resembling a pulldown menu control.

```pascal
PROCEDURE CreateResourcePopup(
				nDialogID     : LONGINT;
				nComponentID  : LONGINT;
				nWidthInChars : INTEGER);
```

```python
def vs.CreateResourcePopup(nDialogID, nComponentID, nWidthInChars):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|The index of the dialog layout containing the control.|
|nComponentID|LONGINT|The index that will identify the control item.|
|nWidthInChars|INTEGER|The width of the displayed text in standard character count. See GetDlgCtrlWidthStdCh.|

## Version
Availability: from Vectorworks 2021

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
