# SetLBItemDisplayType

## Description
Sets item display type for list items in specified column.

```pascal
FUNCTION SetLBItemDisplayType(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER;
				displayType : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemDisplayType(dialogID, componentID, columnIndex, displayType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|
|displayType|INTEGER|the display type to be set (0: Text Only, 1: Icon Only, 3: Text and Icon)|

## Examples
```pascal
BEGIN
	colId0 := InsertLBColumn(dlgId, kLBCtrl, 0, GetPluginString(3010), 40);
	boolD := SetLBControlType(dlgId, kLBCtrl, colId0, 1);
	boolD := SetLBItemDisplayType(dlgId, kLBCtrl, colId0, 0);

ColNum := InsertLBColumn(dlogID,5,0,GetPluginString(6001),50);
temp_b := SetLBControlType(dlogID,5,0,3);
temp_b := SetLBItemDisplayType(dlogID,5,0,1);

BEGIN
	colNum	:= InsertLBColumn(dlogID, itemID,0 ,GetPluginString(3033), 150);
	tempRes := SetLBControlType(dlogID, itemID, colNum, 1);
	tempRes	:= SetLBItemDisplayType(dlogID, itemID, colNum, 0);
```
```python
import vs

# Sets item display type for list items in specified column.
dialogID = 1
componentID = 2
columnIndex = 1
displayType = 0

ok = vs.SetLBItemDisplayType(dialogID, componentID, columnIndex, displayType)
if ok:
    vs.Message('SetLBItemDisplayType succeeded')
else:
    vs.Message('SetLBItemDisplayType failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
