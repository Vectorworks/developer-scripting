# EnableLBSingleLineSelection

## Description
Enables single line only selection.  Multiple selections will not be permitted.

```pascal
FUNCTION EnableLBSingleLineSelection(
				dialogID    : LONGINT;
				componentID : LONGINT;
				enable      : BOOLEAN): BOOLEAN;
```

```python
def vs.EnableLBSingleLineSelection(dialogID, componentID, enable):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|enable|BOOLEAN|determines if single line selection only should be enabled.|

## Examples
```pascal
EnableLBSorting(dlgId, kLBCtrl, FALSE);
{EnableLBColumnLines(dlgId, kLBCtrl, TRUE);} {enables direct edit}
boolD := EnableLBSingleLineSelection(dlgId, kLBCtrl, TRUE);

BEGIN
	EnumerateHeliodons;
	status := EnableLBSingleLineSelection(dialogId, kHeliodonList, TRUE);
	columnIndex := InsertLBColumn(dialogID, kHeliodonList, 0, GetPluginString(3011), 45);
	status := SetLBControlType(dialogID, kHeliodonList, columnIndex, 4);
	status := SetLBItemDisplayType(dialogID, kHeliodonList, columnIndex, 1);
	gFieldsLBImg1 := AddListBrowserImage(dialogID, kHeliodonList, 'Vectorworks/Standard Images/blank.png');

	EnableLBSorting(dlogID, itemID, FALSE);
	EnableLBColumnLines(dlogID, itemID, TRUE);
	tempRes := EnableLBSingleLineSelection(dlogID, itemID, TRUE);
END;
```
```python
import vs

# Enables single line only selection.
dialogID = 1
componentID = 2
enable = True

ok = vs.EnableLBSingleLineSelection(dialogID, componentID, enable)
if ok:
    vs.Message('EnableLBSingleLineSelection succeeded')
else:
    vs.Message('EnableLBSingleLineSelection failed')
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
