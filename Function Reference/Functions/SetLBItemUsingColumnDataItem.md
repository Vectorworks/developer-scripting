# SetLBItemUsingColumnDataItem

## Description
Sets list item data with specified column data item.

```pascal
FUNCTION SetLBItemUsingColumnDataItem(
				dialogID            : LONGINT;
				componentID         : LONGINT;
				itemIndex           : INTEGER;
				subItemIndex        : INTEGER;
				columnDataItemIndex : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemUsingColumnDataItem(dialogID, componentID, itemIndex, subItemIndex, columnDataItemIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|columnDataItemIndex|INTEGER|the column data item with which to set list item data|

## Remarks
(\_c\_, 2015.04.06): this crashes VW 2013 if the cell doesn't have any column data items. Check for the presence of data items in the chosen column using [GetNumLBColumnDataItems](GetNumLBColumnDataItems.md) in order to prevent accidentally using it on cells with no column data items:
```pascal
IF GetNumLBColumnDataItems(dialogID, listBrowserID, columnIndex) > 0 THEN BEGIN
   IF SetLBItemUsingColumnDataItem(dialogID, listBrowserID, rowIndex, columnIndex, columnDataItemIndex) THEN BEGIN
      { ... }
   END;
END;
```

## Examples
```pascal
BEGIN
	columnIndex := InsertLBColumnDataItem(dialogID,kHeliodonList,1, city[i], -1, -1, 0);
	temp := InsertLBItem (dialogID, kHeliodonList, i - 1, city[i]);
	status := SetLBItemUsingColumnDataItem (dialogID, kHeliodonList, i-1, 1, columnIndex);
	column [1] := city[i];
	column [2] := region[i];
	GetVWRString(angleMark, 'Vectorworks/Strings/1010 Dimension Strings.vwstrings', '10');
	column [3] := Concat(Num2Str(2, rotation[i]), angleMark);

BEGIN
	IF value = '' THEN value := ' ';
	IF NOT FindLBColumnDataItem(dialogID, componentID, column, value, ndx) THEN
	ndx := InsertLBColumnDataItem(dialogID, componentID, column, value, 0, 0, 0);
	boo := SetLBItemUsingColumnDataItem(dialogID, componentID, row, column, ndx);
END;

BEGIN
ColNum := InsertLBColumnDataItem(dlogID,5,1,layerNameList[i],-1,-1,0);
temp_i := InsertLBItem (dlogID, 5, i-1, layerNameList[i]);
temp_b := SetLBItemUsingColumnDataItem (dlogID, 5, i-1, 1, ColNum);
IF layerStatusList[i]
	THEN temp_b := SetLBItemUsingColumnDataItem (dlogID, 5, i-1, 0, 0)
	ELSE temp_b := SetLBItemUsingColumnDataItem (dlogID, 5, i-1, 0, 1);
END;
```
```python
import vs

# Sets list item data with specified column data item.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1
columnDataItemIndex = 1

ok = vs.SetLBItemUsingColumnDataItem(dialogID, componentID, itemIndex, subItemIndex, columnDataItemIndex)
if ok:
    vs.Message('SetLBItemUsingColumnDataItem succeeded')
else:
    vs.Message('SetLBItemUsingColumnDataItem failed')
```

## Version
Availability: from VectorWorks 11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
