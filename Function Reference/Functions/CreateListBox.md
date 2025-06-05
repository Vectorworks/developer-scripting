# CreateListBox

## Description
Creates a new list box control in a dialog layout.

```pascal
PROCEDURE CreateListBox(
				dialogID           : LONGINT;
				itemID             : LONGINT;
				widthInCharacters  : LONGINT;
				heightInCharacters : LONGINT);
```

```python
def vs.CreateListBox(dialogID, itemID, widthInCharacters, heightInCharacters):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|widthInCharacters|LONGINT|The width of the control in characters.|
|heightInCharacters|LONGINT|The height of the control in characters.|

## Remarks
This control does not support multiple selections.

## Examples
[DialogLayoutPulldownMenu](examples/DialogLayoutPulldownMenu.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
