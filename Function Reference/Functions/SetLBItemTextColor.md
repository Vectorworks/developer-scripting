# SetLBItemTextColor

## Description
Sets the text color for the specified list browser item.

```pascal
FUNCTION SetLBItemTextColor(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				redIndex     : INTEGER;
				greenIndex   : INTEGER;
				blueIndex    : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemTextColor(dialogID, componentID, itemIndex, subItemIndex, redIndex, greenIndex, blueIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|redIndex|INTEGER|the red component (0 - 255)|
|greenIndex|INTEGER|the green component (0 - 255)|
|blueIndex|INTEGER|the blue component (0 - 255)|

## Examples
```pascal
BEGIN
	LBWorkedInt := InsertLBItem(dialog,kAryCnfgTypePoolLB,			LBLineNumber,	'');
	LBWorkedBool := SetLBItemInfo( dialog, kAryCnfgTypePoolLB, 		LBLineNumber, 	0,	Concat(GetPlugInString(10637)), 0 );
	LBWorkedBool := SetLBItemInfo( dialog, kAryCnfgTypePoolLB, 		LBLineNumber, 	1,	Concat(CurBmprUsrType), 0 );
	LBWorkedBool := SetLBItemTextColor (Dialog,kAryCnfgTypePoolLB,	LBLineNumber,	0,	kBmpAR/257,kBmpAG/257,kBmpAB/257);
	LBWorkedBool := SetLBItemTextColor (Dialog,kAryCnfgTypePoolLB,	LBLineNumber,	1,	kBmpAR/257,kBmpAG/257,kBmpAB/257);
	LBLineNumber := LBLineNumber+1;
END;

END;
boo:=SetLBItemInfo(dialogIDIM, kBrowser, curRow, i, Concat(symCount), 0);
IF gSymInfoList[symCount].isReferenced THEN FOR i:=0 TO GetNumLBColumns(dialogIDIM, kBrowser)-1 DO BEGIN
	boo:=SetLBItemTextStyle(dialogIDIM, kBrowser, curRow, i, kStyleItalic);
	boo:=SetLBItemTextColor(dialogIDIM, kBrowser, curRow, i, 100, 100, 100);
END;

BEGIN
	boo:=SetLBItemTextColor(dialogIDSetup, kBrowserUnused, curRow, kColName, 0, 0, kColorBlueUnused);
	boo:=SetLBItemTextColor(dialogIDSetup, kBrowserUnused, curRow, kColType, 0, 0, kColorBlueUnused);
END;
```
```python
import vs

# Sets the text color for the specified list browser item.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1
redIndex = 1
greenIndex = 1
blueIndex = 1

ok = vs.SetLBItemTextColor(dialogID, componentID, itemIndex, subItemIndex, redIndex, greenIndex, blueIndex)
if ok:
    vs.Message('SetLBItemTextColor succeeded')
else:
    vs.Message('SetLBItemTextColor failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
