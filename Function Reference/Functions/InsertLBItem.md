# InsertLBItem

## Description
Insert an item into the specified list browser control. Returns the index of the created item.

```pascal
FUNCTION InsertLBItem(
				dialogID    : LONGINT;
				componentID : LONGINT;
				itemIndex   : INTEGER;
				itemString  : STRING): INTEGER;
```

```python
def vs.InsertLBItem(dialogID, componentID, itemIndex, itemString):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|index at which the item is to be inserted|
|itemString|STRING|text to set for item|

## Examples
[ComplexDialogLayout4](examples/ComplexDialogLayout4.md)

```pascal
BEGIN
	temp_i := InsertLBItem(IDLabelDialog,kDataBox,i-1,'');
END;

boolD := GetLBItemInfo(dlgId, kLBCtrl, nFloors-1, colId2, elevNameLast, i);
boolD := GetLBItemInfo(dlgId, kLBCtrl, nFloors-1, colId3, flHeightNameLast, i);
IF flName = '' THEN flName := GetPluginString(3012);{'Unspecified' , note - this must be different for other strings}
		{Class}
			rowID := InsertLBItem(dlgId, kLBCtrl, nFloors + 1, Num2Str(0, nFloors + 1));

BEGIN
	columnIndex := InsertLBColumnDataItem(dialogID,kHeliodonList,1, city[i], -1, -1, 0);
	temp := InsertLBItem (dialogID, kHeliodonList, i - 1, city[i]);
	status := SetLBItemUsingColumnDataItem (dialogID, kHeliodonList, i-1, 1, columnIndex);
	column [1] := city[i];
	column [2] := region[i];
	GetVWRString(angleMark, 'Vectorworks/Strings/1010 Dimension Strings.vwstrings', '10');
```
```python
import vs

# Insert an item into the specified list browser control.
dialogID = 1
componentID = 2
itemIndex = 1
itemString = 'Example'

resultN = vs.InsertLBItem(dialogID, componentID, itemIndex, itemString)
vs.Message('InsertLBItem returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
