# GetLBItemTextColor

## Description
Gets the text color for the specified list browser item.

```pascal
FUNCTION GetLBItemTextColor(
				dialogID       : LONGINT;
				componentID    : LONGINT;
				itemIndex      : INTEGER;
				subItemIndex   : INTEGER;
				VAR redIndex   : INTEGER;
				VAR greenIndex : INTEGER;
				VAR blueIndex  : INTEGER): BOOLEAN;
```

```python
def vs.GetLBItemTextColor(dialogID, componentID, itemIndex, subItemIndex):
    return (BOOLEAN, redIndex, greenIndex, blueIndex)
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
	boo:=GetLBItemTextColor(dialogID, itemID, row, kCandlePowerCol, r, g, b);
	isLBRowChanged := FALSE;
	IF (r=TintR) & (g=TintG) & (b=TintB) THEN
		isLBRowChanged:=TRUE;
END;

	symArray[lastPtr-firstPtr+1].cir:=choiceStr;}
	symArray[lastPtr-firstPtr+1].cir:='1';
	boo:=GetLBItemInfo(dialogIDSetup, kBrowserKeyList, lastPtr, kRightColNR, choiceStr, choiceInt);
	symArray[lastPtr-firstPtr+1].nr:=choiceStr;
	boo:=GetLBItemTextColor(dialogIDSetup, kBrowserKeyList, lastPtr, kRightColName, red, green, symArray[lastPtr-firstPtr+1].color);
	IF lastPtr=numRows THEN lastPtr:=lastPtr+1;
END;
```
```python
import vs

# Gets the text color for the specified list browser item.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1

ok, redIndex, greenIndex, blueIndex = vs.GetLBItemTextColor(dialogID, componentID, itemIndex, subItemIndex)
vs.Message('GetLBItemTextColor returned: ' + str((ok, redIndex, greenIndex, blueIndex)))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
