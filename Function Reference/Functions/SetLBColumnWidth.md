# SetLBColumnWidth

## Description
Sets the width of the specified range of columns of the specified list browser control.

```pascal
FUNCTION SetLBColumnWidth(
				dialogID    : LONGINT;
				componentID : LONGINT;
				fromColumn  : INTEGER;
				toColumn    : INTEGER;
				width       : INTEGER): BOOLEAN;
```

```python
def vs.SetLBColumnWidth(dialogID, componentID, fromColumn, toColumn, width):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|fromColumn|INTEGER|first column to be changed|
|toColumn|INTEGER|last column to be changed|
|width|INTEGER|the width of the column in pixels|

## Remarks
On the Mac a List Browser column width of '0' will crash the application or make the dialog window un-exitable (force-quit needed). The same occurs if a user is resetting manually the column width to zero.

This known, the column width zero must be prevented programmatically for safety (VW 12.5-13).

## Examples
```pascal
BEGIN
columnWidth := Str2Int(value);
boo := SetLBColumnWidth(dialogID,componentID,columnIndex,columnIndex, columnWidth);
END;

BEGIN
	boo:=GetLBColumnWidth(dialogID, itemID, colID, curColWidth);
	dataLength:=Len(data);
	IF dataLength>0 THEN colWith:=LB_WidthInPixels(dataLength) ELSE colWith:=1;
	IF colWith>curColWidth THEN boo:=SetLBColumnWidth(dialogID, itemID, colID, colID, colWith);
END;
```
```python
import vs

# Sets the width of the specified range of columns of the specified list
# browser control.
dialogID = 1
componentID = 2
fromColumn = 5
toColumn = 5
width = 3

ok = vs.SetLBColumnWidth(dialogID, componentID, fromColumn, toColumn, width)
if ok:
    vs.Message('SetLBColumnWidth succeeded')
else:
    vs.Message('SetLBColumnWidth failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
