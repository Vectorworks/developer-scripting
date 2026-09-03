# CreateCheckBox2

## Description
Create a checkbox with an icon.

```pascal
PROCEDURE CreateCheckBox2(
				dialogID    : LONGINT;
				itemID      : LONGINT;
				text        : DYNARRAY[] of CHAR;
				iconResPath : DYNARRAY[] of CHAR);
```

```python
def vs.CreateCheckBox2(dialogID, itemID, text, iconResPath):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The ID of the dialog.|
|itemID|LONGINT|The ID of the control.|
|text|DYNARRAY[] of CHAR|The text of this control.|
|iconResPath|DYNARRAY[] of CHAR|The path of the icon resource.|

## Examples
```pascal
CreateCheckBox2(1, 2, text, iconResPath);
```
```python
import vs

# Create a checkbox with an icon.
dialogID = 1
itemID = 2
text = 'Example text'
iconResPath = 'C:/Temp'

vs.CreateCheckBox2(dialogID, itemID, text, iconResPath)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from Vectorworks 2023

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
