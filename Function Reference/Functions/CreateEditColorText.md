# CreateEditColorText

## Description
Create a text box allowing collor and collapsing of text.

```pascal
PROCEDURE CreateEditColorText(
				dialogID       : LONGINT;
				itemID         : LONGINT;
				widthInStdChar : LONGINT;
				heightInLines  : LONGINT);
```

```python
def vs.CreateEditColorText(dialogID, itemID, widthInStdChar, heightInLines):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|widthInStdChar|LONGINT|The width of the displayed text in standard character count. See GetDlgCtrlWidthStdCh.|
|heightInLines|LONGINT|Height of the control in lines.|

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
