# SetLBColumnHeaderToolTip

## Description
Sets the list browser column header's tooltip text.

```pascal
FUNCTION SetLBColumnHeaderToolTip(
				dialogID           : LONGINT;
				componentID        : LONGINT;
				columnIndex        : INTEGER;
				toolTipPrimaryText : STRING;
				toolTipSubText     : STRING): BOOLEAN;
```

```python
def vs.SetLBColumnHeaderToolTip(dialogID, componentID, columnIndex, toolTipPrimaryText, toolTipSubText):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the column index|
|toolTipPrimaryText|STRING|the primary tooltip text|
|toolTipSubText|STRING|the sub tooltip text displayed when the user the command (Mac) or shift (Win) button|

## Examples
```pascal
FOR i:=1 TO kNumFlds DO BEGIN
	tempInt:=InsertLBColumn(dialogIDIM, kBrowser, GetNumLBColumns(dialogIDIM, kBrowser), LIFields[i].colName, 50);
	boo:=SetLBItemDisplayType( dialogIDIM, kBrowser, tempInt, kLBDisplayTextOnly);
	boo:=SetLBControlType(dialogIDIM, kBrowser, tempInt, kLBControlNone);
	boo:=SetLBColumnHeaderToolTip(dialogIDIM, kBrowser, tempInt, LIFields[i].colName, '');
END;

tempInt:=InsertLBColumn(dialogIDSetup, kBrowserKeyList, GetNumLBColumns(dialogIDSetup, kBrowserKeyList), GetStr2(kStr_NonRotate), 28);
	boo:=SetLBItemDisplayType( dialogIDSetup, kBrowserKeyList, tempInt, kLBDisplayImageOnly);
	boo:=SetLBControlType(dialogIDSetup, kBrowserKeyList, tempInt, kLBControlMultiState);
	boo:=SetLBColumnHeaderToolTip(dialogIDSetup, kBrowserKeyList, tempInt, GetStr2(kStr_NR_Tip), GetStr2(kStr_NR_Tip_Long));
```
```python
import vs

# Sets the list browser column header's tooltip text.
dialogID = 1
componentID = 2
columnIndex = 1
toolTipPrimaryText = 'Example text'
toolTipSubText = 'Example text'

ok = vs.SetLBColumnHeaderToolTip(dialogID, componentID, columnIndex, toolTipPrimaryText, toolTipSubText)
if ok:
    vs.Message('SetLBColumnHeaderToolTip succeeded')
else:
    vs.Message('SetLBColumnHeaderToolTip failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
