# SetLBItemTextStyle

## Description
Sets the text style for the specified list browser item.

```pascal
FUNCTION SetLBItemTextStyle(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				textStyle    : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemTextStyle(dialogID, componentID, itemIndex, subItemIndex, textStyle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|textStyle|INTEGER|Plain - 0|Bold - 1|Italic - 2|Underline - 4|Outline - 16 (Mac only)|Shadow - 32 (Mac only)|

## Examples
```pascal
	ResizeLBColumnToData(dialogIDIM, kBrowser, i, data);
END;
boo:=SetLBItemInfo(dialogIDIM, kBrowser, curRow, i, Concat(symCount), 0);
IF gSymInfoList[symCount].isReferenced THEN FOR i:=0 TO GetNumLBColumns(dialogIDIM, kBrowser)-1 DO BEGIN
	boo:=SetLBItemTextStyle(dialogIDIM, kBrowser, curRow, i, kStyleItalic);
	boo:=SetLBItemTextColor(dialogIDIM, kBrowser, curRow, i, 100, 100, 100);
END;

	boo:=DeleteLBItem(dialogIDSetup, kBrowserUsed, delRow)
ELSE
	{Color the row}
	IF IsSpecialItem(locSymName) THEN
		boo:=SetLBItemTextStyle(dialogIDSetup, kBrowserKeyList, curRow-1, kRightColName, 1)
	ELSE
		boo:=SetLBItemTextColor(dialogIDSetup, kBrowserKeyList, curRow-1, kRightColName, 0, 0, kColorBlueUnused);
delRow:=-1;
FOR j:=0 TO GetNumLBItems(dialogIDSetup, kBrowserUnused)-1 DO BEGIN
	boo:=GetLBItemInfo(dialogIDSetup, kBrowserUnused, j, 0, choiceStr, choiceInt);
	IF choiceStr=symName THEN BEGIN
```
```python
import vs

# Sets the text style for the specified list browser item.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1
textStyle = 0

ok = vs.SetLBItemTextStyle(dialogID, componentID, itemIndex, subItemIndex, textStyle)
if ok:
    vs.Message('SetLBItemTextStyle succeeded')
else:
    vs.Message('SetLBItemTextStyle failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
