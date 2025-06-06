# CreateBorderlessBtn

## Description
Creates a borderless button control in a dialog layout.

```pascal
PROCEDURE CreateBorderlessBtn(
				dialogID       : LONGINT;
				itemID         : LONGINT;
				label          : DYNARRAY[] of CHAR;
				iconResPath    : DYNARRAY[] of CHAR;
				isToggleButton : BOOLEAN);
```

```python

def vs.CreateBorderlessBtn(dialogID, itemID, label, iconResPath, isToggleButton):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The ID of the dialog|
|itemID|LONGINT|The ID of the control|
|label|DYNARRAY[] of CHAR|Label of the button. If the label is empty, this button will be a small untitled borderless button.|
|iconResPath|DYNARRAY[] of CHAR|The resource path of the icon|
|isToggleButton|BOOLEAN|A boolean to specify whether this is a toggle button|

## Version
Availability: from Vectorworks 2024

## Category
* [Dialogs - Modern](../Categories/Dialogs - Modern.md)

