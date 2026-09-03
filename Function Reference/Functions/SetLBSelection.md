# SetLBSelection

## Description
Selects the specified range of items within a List Browser dialog control.

```pascal
FUNCTION SetLBSelection(
				dialogID       : LONGINT;
				componentID    : LONGINT;
				firstItemIndex : INTEGER;
				lastItemIndex  : INTEGER;
				select         : BOOLEAN): BOOLEAN;
```

```python
def vs.SetLBSelection(dialogID, componentID, firstItemIndex, lastItemIndex, select):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|firstItemIndex|INTEGER|the first row of the range to select|
|lastItemIndex|INTEGER|the last row of the range to select|
|select|BOOLEAN|select or deselect|

## Examples
```pascal
		LB_SetCell(IDLabelDialog,kDataBox,i-1,1,gDataArr[i,1]);
		LB_SetCell(IDLabelDialog,kDataBox,i-1,2,gDataArr[i,2]);
	END;
	EnableLBColumnLines(IDLabelDialog,kDataBox,TRUE);
	boo := SetLBSelection(IDLabelDialog,kDataBox,0,0,TRUE);
END;

BEGIN
	status := SetLBSelection(dialogID, kHeliodonList, i - 1, i - 1, TRUE);
	status := SetLBItemUsingColumnDataItem(dialogID, kHeliodonList, i - 1, 0, checkedIndex);
END

SetUpListBrowser( 14 );
AddPopUpItems (dlogID, 14, 1);
tempRes := SetLBSelection(dlogID,14,gClassIndex-1,gClassIndex-1,TRUE);
SetItemText(dlogID, 15, gActClassNames [1]);
SetItemText(dlogID, 17, gClassList [1].Description);
EnableItem(dlogID, 9, gActClassChoiceI > 2);
EnableItem(dlogID, 15, gActClassChoiceI > 2);
```
```python
import vs

# Selects the specified range of items within a List Browser dialog control.
dialogID = 1
componentID = 2
firstItemIndex = 1
lastItemIndex = 1
select = True

ok = vs.SetLBSelection(dialogID, componentID, firstItemIndex, lastItemIndex, select)
if ok:
    vs.Message('SetLBSelection succeeded')
else:
    vs.Message('SetLBSelection failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
