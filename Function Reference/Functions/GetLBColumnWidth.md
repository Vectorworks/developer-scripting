# GetLBColumnWidth

## Description
Gets the width of the specified column in the specified list browser control.

```pascal
FUNCTION GetLBColumnWidth(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER;
				VAR width   : INTEGER): BOOLEAN;
```

```python
def vs.GetLBColumnWidth(dialogID, componentID, columnIndex):
    return (BOOLEAN, width)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the column from which to get the width|
|width|INTEGER|width of the column|

## Examples
```pascal
BEGIN
IF GetLBColumnWidth(dialogID,componentID,columnIndex,columnWidth) THEN
	BEGIN
	SetSavedSetting('DialogPositions',Concat(dialogName,'/Comp',Int2Str(componentID),'/Col',Int2Str(columnIndex)),Int2Str(columnWidth));
	END;

LBWorkedBool := GetLBColumnWidth(dialog, kArrayStackLB,0,LBColWdASNum);
LBWorkedBool := GetLBColumnWidth(dialog, kArrayStackLB,1,LBColWdASLet);
LBWorkedBool := GetLBColumnWidth(dialog, kArrayStackLB,2,LBColWdASType);
LBWorkedBool := GetLBColumnWidth(dialog, kArrayStackLB,3,LBColWdASIndTlt);
LBWorkedBool := GetLBColumnWidth(dialog, kArrayStackLB,4,LBColWdASActTlt);

BEGIN
	boo:=GetLBColumnWidth(dialogID, itemID, colID, curColWidth);
	dataLength:=Len(data);
	IF dataLength>0 THEN colWith:=LB_WidthInPixels(dataLength) ELSE colWith:=1;
	IF colWith>curColWidth THEN boo:=SetLBColumnWidth(dialogID, itemID, colID, colID, colWith);
END;
```
```python
import vs

# Gets the width of the specified column in the specified list browser control.
dialogID = 1
componentID = 2
columnIndex = 1

ok, width = vs.GetLBColumnWidth(dialogID, componentID, columnIndex)
vs.Message('GetLBColumnWidth returned: ' + str((ok, width)))
```

## Version
Availability: from Vectorworks14.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
