# InsertLBColumnDataItem

## Description
Inserts column data item with specified data. Returns the index to the newly inserted item.

```pascal
FUNCTION InsertLBColumnDataItem(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER;
				itemString  : STRING;
				imageOn     : INTEGER;
				imageOff    : INTEGER;
				itemData    : LONGINT): INTEGER;
```

```python
def vs.InsertLBColumnDataItem(dialogID, componentID, columnIndex, itemString, imageOn, imageOff, itemData):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the column for which to set the data|
|itemString|STRING|the item text|
|imageOn|INTEGER|the 'on' image list index|
|imageOff|INTEGER|the 'off' image list index|
|itemData|LONGINT|the item user data|

## Remarks
VW2011: It seems to be impossible to fill in a column with the same value with InsertLBColumnDataItem. If you need it, you can use [http://developer.vectorworks.net/index.php?title=VS:SetLBItemInfo SetLBItemInfo] instead.

## Examples
[ComplexDialogLayout4](examples/ComplexDialogLayout4.md)

```pascal
status := SetLBControlType(dialogID, kHeliodonList, columnIndex, 4);
status := SetLBItemDisplayType(dialogID, kHeliodonList, columnIndex, 1);
gFieldsLBImg1 := AddListBrowserImage(dialogID, kHeliodonList, 'Vectorworks/Standard Images/blank.png');
gFieldsLBImg2 := AddListBrowserImage(dialogID, kHeliodonList, 'Vectorworks/Standard Images/whitecheckmark.png');
uncheckedIndex := InsertLBColumnDataItem(dialogID, kHeliodonList, 0, 'False', gFieldsLBImg1, -1, 0);
checkedIndex := InsertLBColumnDataItem(dialogID, kHeliodonList, 0, 'True',  gFieldsLBImg2, -1, 1);

BEGIN
	IF value = '' THEN value := ' ';
	IF NOT FindLBColumnDataItem(dialogID, componentID, column, value, ndx) THEN
	ndx := InsertLBColumnDataItem(dialogID, componentID, column, value, 0, 0, 0);
	boo := SetLBItemUsingColumnDataItem(dialogID, componentID, row, column, ndx);
END;

ColNum := InsertLBColumnDataItem(dlogID,5,0,kT,kImageCheck,-1,1);
ColNum := InsertLBColumnDataItem(dlogID,5,0,kF,kImageBlank,-1,0);
```
```python
import vs

# Inserts column data item with specified data.
dialogID = 1
componentID = 2
columnIndex = 1
itemString = 'Example'
imageOn = 3
imageOff = 10
itemData = 1

resultN = vs.InsertLBColumnDataItem(dialogID, componentID, columnIndex, itemString, imageOn, imageOff, itemData)
vs.Message('InsertLBColumnDataItem returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
