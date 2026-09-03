# GetNumLBColumns

## Description
Gets the number of columns in the specified list browser control.

```pascal
FUNCTION GetNumLBColumns(
				dialogID    : LONGINT;
				componentID : LONGINT): INTEGER;
```

```python
def vs.GetNumLBColumns(dialogID, componentID):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|

## Examples
```pascal
BEGIN
	NumCol := GetNumLBColumns(dialogID,componentID)-1;
	For columnIndex := 0 to NumCol DO
		BEGIN
		IF GetLBColumnWidth(dialogID,componentID,columnIndex,columnWidth) THEN
			BEGIN

{//////// Create Columns ////////}
{Position}
gIdxSelect:=InsertLBColumn(dialogIDFilters, kBrowserPosition, GetNumLBColumns(dialogIDFilters, kBrowserPosition), '', 25);
boo:=SetLBItemDisplayType(dialogIDFilters, kBrowserPosition, gIdxSelect, kLBDisplayImageOnly);
boo:=SetLBControlType(dialogIDFilters, kBrowserPosition, gIdxSelect, kLBControlMultiState);

	boo:=SetLBItemInfo(dialogIDIM, kBrowser, curRow, i, data, 0);
	ResizeLBColumnToData(dialogIDIM, kBrowser, i, data);
END;
boo:=SetLBItemInfo(dialogIDIM, kBrowser, curRow, i, Concat(symCount), 0);
IF gSymInfoList[symCount].isReferenced THEN FOR i:=0 TO GetNumLBColumns(dialogIDIM, kBrowser)-1 DO BEGIN
	boo:=SetLBItemTextStyle(dialogIDIM, kBrowser, curRow, i, kStyleItalic);
	boo:=SetLBItemTextColor(dialogIDIM, kBrowser, curRow, i, 100, 100, 100);
END;
```
```python
import vs

# Gets the number of columns in the specified list browser control.
dialogID = 1
componentID = 2

count = vs.GetNumLBColumns(dialogID, componentID)
vs.Message('GetNumLBColumns returned: ' + str(count))
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
