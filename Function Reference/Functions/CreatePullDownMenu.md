# CreatePullDownMenu

## Description
Creates a new pulldown menu control in a dialog layout.

```pascal
PROCEDURE CreatePullDownMenu(
				dialogID          : LONGINT;
				itemID            : LONGINT;
				widthInCharacters : LONGINT);
```

```python
def vs.CreatePullDownMenu(dialogID, itemID, widthInCharacters):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|widthInCharacters|LONGINT|The width of the control in characters.|

## Examples
[DialogLayoutPulldownMenu](examples/DialogLayoutPulldownMenu.md)

```pascal
{* Create the control items *}
	CreateStaticText (dialogID, 4, GetPlugInString (3004), 45);
	CreateStaticText (dialogID, 5, GetPlugInString (3005), -1);
	CreatePullDownMenu (dialogID, 6, 32);
	CreateStaticText (dialogID, 7, GetPlugInString (3006), -1);
	CreatePullDownMenu (dialogID, 8, 32);

{* Create the control items *}
	CreateStaticText (dialogID, 4, GetPlugInString (3004), 45);
	CreateStaticText (dialogID, 5, GetPlugInString (3005), labelWidth);
	CreatePullDownMenu (dialogID, 6, 32);
	CreateStaticText (dialogID, 7, GetPlugInString (3006), labelWidth);
	CreatePullDownMenu (dialogID, 8, 32);
	CreateStaticText (dialogID, 9, GetPlugInString (3021), labelWidth);
	CreatePullDownMenu (dialogID, 10, 32);

{*Symbol Folder *}
CreateStaticText (dialogID, 5, GetPlugInString (3005), -1);
CreatePullDownMenu (dialogID, 6, 32);
```
```python
import vs

# Creates a new pulldown menu control in a dialog layout.
dialogID = 1
itemID = 2
widthInCharacters = 3

vs.CreatePullDownMenu(dialogID, itemID, widthInCharacters)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
