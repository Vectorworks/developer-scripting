# CreateCheckBoxGroupBox

## Description
Creates a checkbox group box.  The checkbox will have name as its label.  If hasFrame is true, the group will have a box drawn around it like a regular group box.

```pascal
PROCEDURE CreateCheckBoxGroupBox(
				dialogID : LONGINT;
				itemID   : LONGINT;
				name     : STRING;
				hasFrame : BOOLEAN);
```

```python
def vs.CreateCheckBoxGroupBox(dialogID, itemID, name, hasFrame):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the dialog|
|itemID|LONGINT|ID of the checkbox group box|
|name|STRING|Title that appears in the checkbox group box|
|hasFrame|BOOLEAN|True if the group box has a frame around it; false otherwise|

## Remarks
On VW 12.5.1 Win the border must be set to TRUE. If the border is set to FALSE the application crashes by clicking the checkBoxGroupBox.

On VW 2016 Win the name parameter must have at least 2 characters or the checkbox will not be drawn.

## Examples
mplexDialogLayout2}}

## Version
Availability: from VectorWorks10.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
