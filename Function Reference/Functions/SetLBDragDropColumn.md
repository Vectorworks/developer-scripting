# SetLBDragDropColumn

## Description
Sets the drag and drop column.

```pascal
FUNCTION SetLBDragDropColumn(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER): BOOLEAN;
```

```python
def vs.SetLBDragDropColumn(dialogID, componentID, columnIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the column index|

## Examples
```pascal
cnt := InsertLBColumn        (AddEditLegend, kFieldsLB, kColNumber, GetPlugInString(10004), 30);
boo := SetLBControlType      (AddEditLegend, kFieldsLB, kColNumber, kLBNumber);
boo := SetLBItemDisplayType  (AddEditLegend, kFieldsLB, kColNumber, kTextOnly);
boo := EnableLBDragAndDrop   (AddEditLegend, kFieldsLB, TRUE);
boo := SetLBDragDropColumn   (AddEditLegend, kFieldsLB, kColNumber);

LBWorkedBool := SetLBControlType (dialog,	kArrayStackLB,	0, kNumberLBCtrlType);
LBWorkedBool := EnableLBDragAndDrop(dialog,	kArrayStackLB,	TRUE);
LBWorkedBool := SetLBDragDropColumn(dialog,	kArrayStackLB,	0);
EnableLBSorting(dialog,						kArrayStackLB,	FALSE);

TmpInt := InsertLBColumn (dialog, kFrntMltColBrowser, 2, GetPlugInString(11163), 60 );		{2 - Color}
bFlipTexture := SetLBControlType (dialog, kFrntMltColBrowser, 0, kNumberLBCtrlType);
EnableLBSorting(dialog, kFrntMltColBrowser, FALSE);
bFlipTexture := EnableLBDragAndDrop(dialog, kFrntMltColBrowser, TRUE);
bFlipTexture := SetLBDragDropColumn(dialog, kFrntMltColBrowser, 0);
DiaColorCountInc := gDiaClrCountTtl;
LBClrCountTtl := 0;
While DiaColorCountInc <> 0 DO
	BEGIN
```
```python
import vs

# Sets the drag and drop column.
dialogID = 1
componentID = 2
columnIndex = 1

ok = vs.SetLBDragDropColumn(dialogID, componentID, columnIndex)
if ok:
    vs.Message('SetLBDragDropColumn succeeded')
else:
    vs.Message('SetLBDragDropColumn failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
