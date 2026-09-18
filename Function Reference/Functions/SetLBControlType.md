# SetLBControlType

## Description
Sets control type for column.

```pascal
FUNCTION SetLBControlType(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER;
				controlType : INTEGER): BOOLEAN;
```

```python
def vs.SetLBControlType(dialogID, componentID, columnIndex, controlType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|
|controlType|INTEGER|the control type to be set (1: Static, 2: Radio, 3: Multi State, 4: Single Instance Icon [See Organization Dialog active element column], 5: Static Icon, 6: Number, 7: Multiple Icons)|

## Examples
```pascal
BEGIN
	FirstCol := InsertLBColumn(IDLabelDialog,kDataBox,0,'',35);
	boo := SetLBControlType(IDLabelDialog,kDataBox,0,1);
	SecondCol := InsertLBColumn(IDLabelDialog,kDataBox,1,GetPluginString(9114),100);
	boo := SetLBControlType(IDLabelDialog,kDataBox,1,1);
	ThirdCol := InsertLBColumn(IDLabelDialog,kDataBox,2,GetPluginString(9115),600);
	boo := SetLBControlType(IDLabelDialog,kDataBox,2,1);

BEGIN
	colId0 := InsertLBColumn(dlgId, kLBCtrl, 0, GetPluginString(3010), 40);
	boolD := SetLBControlType(dlgId, kLBCtrl, colId0, 1);
	boolD := SetLBItemDisplayType(dlgId, kLBCtrl, colId0, 0);

BEGIN
	EnumerateHeliodons;
	status := EnableLBSingleLineSelection(dialogId, kHeliodonList, TRUE);
	columnIndex := InsertLBColumn(dialogID, kHeliodonList, 0, GetPluginString(3011), 45);
	status := SetLBControlType(dialogID, kHeliodonList, columnIndex, 4);
	status := SetLBItemDisplayType(dialogID, kHeliodonList, columnIndex, 1);
	gFieldsLBImg1 := AddListBrowserImage(dialogID, kHeliodonList, 'Vectorworks/Standard Images/blank.png');
	gFieldsLBImg2 := AddListBrowserImage(dialogID, kHeliodonList, 'Vectorworks/Standard Images/whitecheckmark.png');
	uncheckedIndex := InsertLBColumnDataItem(dialogID, kHeliodonList, 0, 'False', gFieldsLBImg1, -1, 0);
```
```python
import vs

# Sets control type for column.
dialogID = 1
componentID = 2
columnIndex = 1
controlType = 0

ok = vs.SetLBControlType(dialogID, componentID, columnIndex, controlType)
if ok:
    vs.Message('SetLBControlType succeeded')
else:
    vs.Message('SetLBControlType failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
