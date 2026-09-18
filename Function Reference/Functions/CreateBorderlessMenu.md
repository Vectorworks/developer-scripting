# CreateBorderlessMenu

## Description
Creates a borderless menu button control in a dialog layout.

```pascal
PROCEDURE CreateBorderlessMenu(
				dialogID    : LONGINT;
				itemID      : LONGINT;
				label       : DYNARRAY[] of CHAR;
				iconResPath : DYNARRAY[] of CHAR);
```

```python

def vs.CreateBorderlessMenu(dialogID, itemID, label, iconResPath):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The ID of the dialog|
|itemID|LONGINT|The ID of the control|
|label|DYNARRAY[] of CHAR|Label of the button. If the label is empty, this button will be a small untitled borderless menu button.|
|iconResPath|DYNARRAY[] of CHAR|The resource path of the icon|

## Examples
```pascal
CreateBorderlessMenu(1, 2, label, iconResPath);
```
```python
import vs

# Creates a borderless menu button control in a dialog layout.
dialogID = 1
itemID = 2
label = 'Example text'
iconResPath = 'C:/Temp'

vs.CreateBorderlessMenu(dialogID, itemID, label, iconResPath)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from Vectorworks 2024

## Category
* [Dialogs - Modern](../Categories/Dialogs - Modern.md)
