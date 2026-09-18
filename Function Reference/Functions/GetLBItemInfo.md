# GetLBItemInfo

## Description
Gets string and image information for a specified item of a List Browser control.

```pascal
FUNCTION GetLBItemInfo(
				dialogID       : LONGINT;
				componentID    : LONGINT;
				itemIndex      : INTEGER;
				subItemIndex   : INTEGER;
				VAR itemString : STRING;
				VAR imageIndex : INTEGER): BOOLEAN;
```

```python
def vs.GetLBItemInfo(dialogID, componentID, itemIndex, subItemIndex):
    return (BOOLEAN, itemString, imageIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the item index|
|subItemIndex|INTEGER|the subitem index|
|itemString|STRING|the item text|
|imageIndex|INTEGER|the item image list index|

## Remarks
* itemIndex = row
* subItemIndex = column

## Examples
```pascal
BEGIN
	boolD := GetLBItemInfo(dlgId, kLBCtrl, nFloors-1, colId1, clNameLast, i);
	boolD := GetLBItemInfo(dlgId, kLBCtrl, nFloors-1, colId2, elevNameLast, i);
	boolD := GetLBItemInfo(dlgId, kLBCtrl, nFloors-1, colId3, flHeightNameLast, i);
	IF flName = '' THEN flName := GetPluginString(3012);{'Unspecified' , note - this must be different for other strings}
			{Class}

BEGIN
	status := GetLBItemInfo(dialogID, kHeliodonList, i, 0, tempString, temp);
	i := i + 1;
END;

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

# Gets string and image information for a specified item of a List Browser
# control.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1

ok, itemString, imageIndex = vs.GetLBItemInfo(dialogID, componentID, itemIndex, subItemIndex)
vs.Message('GetLBItemInfo returned: ' + str((ok, itemString, imageIndex)))
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
