# GetNumSelectedLBItems

## Description
Returns the number of selected list browser items.

```pascal
FUNCTION GetNumSelectedLBItems(
				dialogID    : LONGINT;
				componentID : LONGINT): INTEGER;
```

```python
def vs.GetNumSelectedLBItems(dialogID, componentID):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|

## Examples
```pascal
IF GetLBItemText(dialogIDFilters, item, LBRow, gIdxSelect) = 'off' THEN
	tempInt:=1
ELSE
	tempInt:=0;
LBSelSize:=GetNumSelectedLBItems(dialogIDFilters, item);
IF LBSelSize>=0 THEN BEGIN
	FOR i:=GetNumLBItems(dialogIDFilters, item)-1 DOWNTO 0 DO BEGIN
		IF IsLBItemSelected(dialogIDFilters, item, i) THEN BEGIN
			boo:=SetLBItemUsingColumnDataItem(dialogIDFilters, item, i, gIdxSelect, tempInt);

firstSelected:=true;
FOR i:=1 TO GetNumLBItems(dialogIDIM, kBrowser) DO BEGIN
	IF IsLBItemSelected(dialogIDIM, kBrowser, i-1) THEN BEGIN
		choiceStr:=GetLBItemText(dialogIDIM, kBrowser, i-1, 0);
		IF GetNumSelectedLBItems(dialogIDIM, kBrowser)=1 THEN BEGIN
			UpdateSymbolDisplayControl(dialogIDIMEdit,kSymbolDisp,choiceStr,0,2);
			SetItemText(dialogIDIMEdit, kStaticSymName, choiceStr);
		END

BEGIN
	{//////// Determine Insertion Point ////////}
	insertionPoint:=0;
	selSize:=GetNumSelectedLBItems(dialogIDIM, kBrowser);
	IF selSize>0 THEN BEGIN
		WHILE (NOT IsLBItemSelected(dialogIDIM, kBrowser, insertionPoint)) DO BEGIN
			insertionPoint:=insertionPoint+1;
		END;
```
```python
import vs

# Returns the number of selected list browser items.
dialogID = 1
componentID = 2

count = vs.GetNumSelectedLBItems(dialogID, componentID)
vs.Message('GetNumSelectedLBItems returned: ' + str(count))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
