# InsertLBColumn

## Description
Inserts a column into the specified list browser control. Returns index of created column.

```pascal
FUNCTION InsertLBColumn(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				columnIndex  : INTEGER;
				headerString : STRING;
				width        : INTEGER): INTEGER;
```

```python
def vs.InsertLBColumn(dialogID, componentID, columnIndex, headerString, width):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|index at which the column is to be inserted|
|headerString|STRING|text to set as column header|
|width|INTEGER|the width of the column in pixels|

## Remarks
width is specified in pixles

If you recursively use '0' as 'columnIndex' where to insert the new column, all column headers after the second will center the text label. Moreover they cannot be justified any longer.

If you insert an image to the List Browser, the second column header unexpectedly will display an image instead of text.

So don't use recursively zero for creating new columns. The issue disturbs quite a lot if you are loading columns from XML files, since the element reading starts from the end, so you'd like to add the columns always at top of the list.

(VW 12 - 13)

## Examples
[ComplexDialogLayout4](examples/ComplexDialogLayout4.md)

```pascal
BEGIN
	FirstCol := InsertLBColumn(IDLabelDialog,kDataBox,0,'',35);
	boo := SetLBControlType(IDLabelDialog,kDataBox,0,1);
	SecondCol := InsertLBColumn(IDLabelDialog,kDataBox,1,GetPluginString(9114),100);
	boo := SetLBControlType(IDLabelDialog,kDataBox,1,1);
	ThirdCol := InsertLBColumn(IDLabelDialog,kDataBox,2,GetPluginString(9115),600);

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
```
```python
import vs

# Inserts a column into the specified list browser control.
dialogID = 1
componentID = 2
columnIndex = 1
headerString = 'Example'
width = 3

resultN = vs.InsertLBColumn(dialogID, componentID, columnIndex, headerString, width)
vs.Message('InsertLBColumn returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
