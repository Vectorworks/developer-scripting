# CreateStaticText

## Description
Creates a new static text field control in a dialog layout.

To allow the control to size automatically to the text width, pass -1 as the width parameter of the control.

```pascal
PROCEDURE CreateStaticText(
				dialogID          : LONGINT;
				itemID            : LONGINT;
				text              : STRING;
				widthInCharacters : LONGINT);
```

```python
def vs.CreateStaticText(dialogID, itemID, text, widthInCharacters):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index that will identify the control item.|
|text|STRING|The display text for the control.|
|widthInCharacters|LONGINT|The width of the control in characters.|

## Remarks
To do multi-line static text, a fixed width for the control must be provided to control wrapping. The Layout Manager will determine the height of the control which will contain the entire string. If Chr(13)’s are included in the string, the string will be wrapped at the right edge of the control and broken at the Chr(13)’s as well.

If you are overlaying a StaticText control over an image e.g in an About My Great Plugin... dialog you'l find that on Windows your text background s filled in gray behind the text instead of being transparent so your image shows thru. There is a low-level fix for this in Vectorworks. Just set the color of the text to 1,1,1 instead of 0,0,0 using SetStaticTextColor(dialogID, componentID, red, green, blue); Conrad.

## Examples
*[ComplexDialogLayout](examples/ComplexDialogLayout.md)
*[ComplexDialogLayout2](examples/ComplexDialogLayout2.md)

```pascal
{* Create dialog control items *}
{* Arc Length *}
CreateStaticText (dialogID, 3, fieldS [4], -1);
CreateEditText (dialogID, 4, '', 20);

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
```
```python
import vs

# Creates a new static text field control in a dialog layout.
dialogID = 1
itemID = 2
text = 'Example text'
widthInCharacters = 3

vs.CreateStaticText(dialogID, itemID, text, widthInCharacters)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
