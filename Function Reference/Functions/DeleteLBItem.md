# DeleteLBItem

## Description
Deletes an item from the specified list browser control.

```pascal
FUNCTION DeleteLBItem(
				dialogID    : LONGINT;
				componentID : LONGINT;
				itemIndex   : INTEGER): BOOLEAN;
```

```python
def vs.DeleteLBItem(dialogID, componentID, itemIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the index of the item to delete|

## Examples
```pascal
BEGIN
	nFloors := nFloors - 1;{deletes last floor  == row}
	boolD := DeleteLBItem(dlgId,  kLBCtrl, nFloors);
END;

TempHand := GetObject(gLegendName);
DelObj(TempHand);
For cnt := 1 to gNumLabelLegends DO
	IF LegendSymbol[cnt,1].LegendSymName = gLegendName THEN LegendSymbol[cnt,1].LegendSymName := '';
boo := DeleteLBItem(ChooseLegend, kChooseLB,rowID);
boo := FindLBColumnDataItem(ChooseLegend, kChooseLB, kColLegendName, gLegendName ,rowID);
boo := RemoveLBColumnDataItem(ChooseLegend, kChooseLB, kColLegendName, rowID);
LB_GetSelChoice(ChooseLegend, kChooseLB, kColLegendName, rowID,textStr);
IF rowID = -1 THEN

											IF NumDefBmprsB < 1 THEN NumDefBmprsB := 1;
											SetItemText (dialog,kBmpBCountLab, Concat(GetPluginString(10090),' (',CurBmprBUsrType,'):'));
											SetItemText (dialog,kBmpBCount,Concat(NumDefBmprsB));
										END;
	LBWorkedBool := DeleteLBItem (dialog,kArrayStackLB,i);
	LastDeleted := i;
	Done := TRUE;
END;
```
```python
import vs

# Deletes an item from the specified list browser control.
dialogID = 1
componentID = 2
itemIndex = 1

ok = vs.DeleteLBItem(dialogID, componentID, itemIndex)
if ok:
    vs.Message('DeleteLBItem succeeded')
else:
    vs.Message('DeleteLBItem failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
