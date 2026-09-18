# EnsureLBItemIsVisible

## Description
Ensures the element at the given row index is visible in the specified list browser.

```pascal
FUNCTION EnsureLBItemIsVisible(
				dialogID    : LONGINT;
				componentID : LONGINT;
				index       : INTEGER): BOOLEAN;
```

```python
def vs.EnsureLBItemIsVisible(dialogID, componentID, index):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|index|INTEGER|the row index|

## Examples
```pascal
	Record(symH, kLIMRecName);
	boo:=AddSymbolToBrowser(symH);
	insertionPoint:=GetNumLBItems(dialogIDIM, kBrowser)-1;
	MarkRowChanged(insertionPoint);
	boo:=EnsureLBItemIsVisible(dialogIDIM, kBrowser, insertionPoint);
	gDoRefresh:=TRUE;
	{//////// Add LI Record to existing symbols ////////}
	ForEachObject(AddLInfo, (S=symDName) & (NOT (R IN [kLIRecName])));
END;

	curRow:=InsertLBItem(dialogIDSetup, kBrowserKeyList, insertionPoint, '-');
	boo:=SetLBItemInfo(dialogIDSetup, kBrowserKeyList, insertionPoint, kRightColName, choiceStr, -1);
	boo:=SetLBItemTextStyle(dialogIDSetup, kBrowserKeyList, insertionPoint, kRightColName, 1);
	boo:=EnsureLBItemIsVisible(dialogIDSetup, kBrowserKeyList, insertionPoint);
END;
```
```python
import vs

# Ensures the element at the given row index is visible in the specified list
# browser.
dialogID = 1
componentID = 2
index = 1

ok = vs.EnsureLBItemIsVisible(dialogID, componentID, index)
if ok:
    vs.Message('EnsureLBItemIsVisible succeeded')
else:
    vs.Message('EnsureLBItemIsVisible failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
