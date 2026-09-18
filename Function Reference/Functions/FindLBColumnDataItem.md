# FindLBColumnDataItem

## Description
Finds the column data item with the specified text.

```pascal
FUNCTION FindLBColumnDataItem(
				dialogID                : LONGINT;
				componentID             : LONGINT;
				columnIndex             : INTEGER;
				itemString              : STRING;
				VAR columnDataItemIndex : INTEGER): BOOLEAN;
```

```python
def vs.FindLBColumnDataItem(dialogID, componentID, columnIndex, itemString):
    return (BOOLEAN, columnDataItemIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|
|itemString|STRING|the text to find|
|columnDataItemIndex|INTEGER|the index at which the text was found|

## Examples
```pascal
BEGIN
	IF value = '' THEN value := ' ';
	IF NOT FindLBColumnDataItem(dialogID, componentID, column, value, ndx) THEN
	ndx := InsertLBColumnDataItem(dialogID, componentID, column, value, 0, 0, 0);
	boo := SetLBItemUsingColumnDataItem(dialogID, componentID, row, column, ndx);
END;

BEGIN
index := ParmStackOrder[labelIndex, orderNum];
IF index <> 0 THEN
	IF FindLBColumnDataItem(AddEditLegend, kFieldsLB, kColAttribute, ParmList[ index ].LocalFldName, int) THEN
		BEGIN
		LB_SetCell(AddEditLegend, kFieldsLB, int, kColNumber, Concat(orderNum));
		numberedFields := orderNum+1;
		END;
```
```python
import vs

# Finds the column data item with the specified text.
dialogID = 1
componentID = 2
columnIndex = 1
itemString = 'Example'

ok, columnDataItemIndex = vs.FindLBColumnDataItem(dialogID, componentID, columnIndex, itemString)
vs.Message('FindLBColumnDataItem returned: ' + str((ok, columnDataItemIndex)))
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
