# CreateRadioButtonGroupBox

## Description
Creates a radio button group box.  The radio button will have name as its label.  If hasFrame is true, the group will have a box drawn around it like a regular group box.

```pascal
PROCEDURE CreateRadioButtonGroupBox(
				dialogID : LONGINT;
				itemID   : LONGINT;
				name     : STRING;
				hasFrame : BOOLEAN);
```

```python
def vs.CreateRadioButtonGroupBox(dialogID, itemID, name, hasFrame):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the dialog|
|itemID|LONGINT|ID of the radio button group box|
|name|STRING|Title that appears in the radio button group box|
|hasFrame|BOOLEAN|True whether the group has a frame; false otherwise|

## Version
Availability: from VectorWorks10.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
