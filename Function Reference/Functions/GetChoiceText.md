# GetChoiceText

## Description
Using the index, gets the text of the menu item of the given component.

```pascal
PROCEDURE GetChoiceText(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				VAR itemText : STRING);
```

```python
def vs.GetChoiceText(dialogID, componentID, itemIndex):
    return itemText
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The dialog identifier given by CreateLayout or CreateResizableLayout|
|componentID|LONGINT|The identifier of the control that contains the menu items from which the text will be retrieved from.|
|itemIndex|INTEGER|The item index that contains the desired text.|
|itemText|STRING|The text of the item.|

## Examples
```pascal
GetChoiceText(dialogID, popupID, 1, strg);
ColorIndexToRGB(Str2Num(strg), r2, g2, b2);
diff := ColorDiff(r1, g1, b1, r2, g2, b2);
colorStr := strg;
GetChoiceCount(dialogID, popupID, itemCount);

BEGIN
	GetChoiceText(dialog1, kPopup7, cnt, gPopup7Str);
	IF gPopup7Str = gLocShapeSeries THEN
	BEGIN
		{AlrtDialog( Concat('### GetStructShape::Setup - gLocShapeSeries found: ', gLocShapeSeries) );}
		gPopup7Int := cnt;

BEGIN
	GetChoiceText( IDLabelDialog, kLabelClass, i, tmpStr );
	IF tmpStr = DefaultClass THEN
	BEGIN
		defaultClassFound := TRUE;
	END;
```
```python
import vs

# Using the index, gets the text of the menu item of the given component.
dialogID = 1
componentID = 2
itemIndex = 1

result = vs.GetChoiceText(dialogID, componentID, itemIndex)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
