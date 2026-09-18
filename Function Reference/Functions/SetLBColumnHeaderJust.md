# SetLBColumnHeaderJust

## Description
Sets the specified column header's justification.

```pascal
FUNCTION SetLBColumnHeaderJust(
				dialogID      : LONGINT;
				componentID   : LONGINT;
				columnIndex   : INTEGER;
				justification : INTEGER): BOOLEAN;
```

```python
def vs.SetLBColumnHeaderJust(dialogID, componentID, columnIndex, justification):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the column index|
|justification|INTEGER|Left - 1|Center - 2|Right - 3|

## Examples
```pascal
{Key List}
IF EnableLBDragAndDrop(dialogIDSetup, kBrowserKeyList, TRUE) THEN BEGIN
	tempInt:=InsertLBColumn(dialogIDSetup, kBrowserKeyList, GetNumLBColumns(dialogIDSetup, kBrowserKeyList), '#', 30);
	boo:=SetLBColumnHeaderJust(dialogIDSetup, kBrowserKeyList, tempInt, 1);
	boo:=SetLBItemDisplayType(dialogIDSetup, kBrowserKeyList, tempInt, kLBDisplayTextOnly);
	boo:=SetLBControlType(dialogIDSetup, kBrowserKeyList, tempInt, kLBControlNumber);
	boo:=SetLBDragDropColumn(dialogIDSetup, kBrowserKeyList, tempInt);
END;
```
```python
import vs

# Sets the specified column header's justification.
dialogID = 1
componentID = 2
columnIndex = 1
justification = 3

ok = vs.SetLBColumnHeaderJust(dialogID, componentID, columnIndex, justification)
if ok:
    vs.Message('SetLBColumnHeaderJust succeeded')
else:
    vs.Message('SetLBColumnHeaderJust failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
