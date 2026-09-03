# IsLBItemSelected

## Description
Determines if the specified item is currently selected.

```pascal
FUNCTION IsLBItemSelected(
				dialogID    : LONGINT;
				componentID : LONGINT;
				itemIndex   : INTEGER): BOOLEAN;
```

```python
def vs.IsLBItemSelected(dialogID, componentID, itemIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row number|

## Examples
```pascal
curSel := -1;
nSelectedFloor := -1;
isSelected := FALSE;
FOR cnt := 1 TO maxFloors DO
	IF IsLBItemSelected(dlgId, kLBCtrl, cnt-1) THEN
	BEGIN
		curSel := cnt-1;
		boolD := GetLBItemInfo(dlgId, kLBCtrl, curSel, colId1, strClass, int2);
		boolD := GetLBItemInfo(dlgId, kLBCtrl, curSel, colId2, strElevation, int2);
		boolD := GetLBItemInfo(dlgId, kLBCtrl, curSel, colId3, strThickness, int2);
		boolD := GetLBItemInfo(dlgId, kLBCtrl, curSel, colId4, lString, int2);

BEGIN
	i := 0;
	WHILE ((NOT IsLBItemSelected(dialogID, kHeliodonList, i)) & (i < numHeliodons)) DO
	BEGIN
		i := i + 1;
	END;

BEGIN
	rowID := -1; {the standard value for nothing selected}
	for cnt := 0 to GetNumLBItems(dialogID, controlID) - 1 do BEGIN
		if IsLBItemSelected(dialogID, controlID, cnt) then BEGIN
			rowID := cnt;
			boo := GetLBItemInfo(dialogID, controlID, cnt, columnID, textStr, cnt);
			cnt := GetNumLBItems(dialogID, controlID);
		END;
```
```python
import vs

# Determines if the specified item is currently selected.
dialogID = 1
componentID = 2
itemIndex = 1

ok = vs.IsLBItemSelected(dialogID, componentID, itemIndex)
if ok:
    vs.Message('IsLBItemSelected succeeded')
else:
    vs.Message('IsLBItemSelected failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
