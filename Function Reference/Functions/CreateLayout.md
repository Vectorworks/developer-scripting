# CreateLayout

## Description
Creates a new custom dialog layout. After the layout is created, control items for the dialog can be added to the layout.

```pascal
FUNCTION CreateLayout(
				dialogTitle       : STRING;
				hasHelp           : BOOLEAN;
				defaultButtonName : STRING;
				cancelButtonName  : STRING): LONGINT;
```

```python
def vs.CreateLayout(dialogTitle, hasHelp, defaultButtonName, cancelButtonName):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogTitle|STRING|Title of the dialog.|
|hasHelp|BOOLEAN|Enables help text for the dialog.|
|defaultButtonName|STRING|Text displayed in the default button of the dialog.|
|cancelButtonName|STRING|Text displayed in the cancel button of the dialog.|

## Remarks
Creates a dialog with a default button, cancel button, and a help box. If you do not want a button created then pass an empty string.

Note that when you start creating controls, you should stick to IDs that are less than 500. Using IDs >= 500 will sometimes work, but sometimes they will not. (Layout Manager writes its own information into whatever structure it's using, in the 500+ range, and this "might" over-write control indexes.)

It is possible to place a control next to the OK and Cancel button. To do this, give that control id 12605. It is not neccesary to add this control to the layout, this is done automatically (see Example 2 below).

## Examples
[DialogLayoutPulldownMenu](examples/DialogLayoutPulldownMenu.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
