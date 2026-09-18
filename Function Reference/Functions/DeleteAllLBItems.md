# DeleteAllLBItems

## Description
Deletes all list browser items.

```pascal
FUNCTION DeleteAllLBItems(
				dialogID    : LONGINT;
				componentID : LONGINT): BOOLEAN;
```

```python
def vs.DeleteAllLBItems(dialogID, componentID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|

## Examples
```pascal
BEGIN
	tempResBool := DeleteAllLBItems(dialogID, itemID);
	CASE choice OF
		1: BEGIN
			FOR i := 1 TO gNumClasses DO
			BEGIN

GetSelectedChoiceInfo(dialog,kSprtPopUp,	0,	gListChoiceArSpndx, gListChoiceArSptext);
LBWorkedBool := DeleteAllLBItems (dialog,kAryCnfgTypePoolLB);
```
```python
import vs

# Deletes all list browser items.
dialogID = 1
componentID = 2

ok = vs.DeleteAllLBItems(dialogID, componentID)
if ok:
    vs.Message('DeleteAllLBItems succeeded')
else:
    vs.Message('DeleteAllLBItems failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
