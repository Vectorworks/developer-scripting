# GetLBColumnHeaderToolTip

## Description
Gets the list browser column header's tooltip text.

```pascal
FUNCTION GetLBColumnHeaderToolTip(
				dialogID               : LONGINT;
				componentID            : LONGINT;
				columnIndex            : INTEGER;
				VAR toolTipPrimaryText : STRING;
				VAR toolTipSubText     : STRING): BOOLEAN;
```

```python
def vs.GetLBColumnHeaderToolTip(dialogID, componentID, columnIndex):
    return (BOOLEAN, toolTipPrimaryText, toolTipSubText)
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
resultOK := GetLBColumnHeaderToolTip(1, 2, 3, 'Example', 'Example');
```
```python
import vs

# Gets the list browser column header's tooltip text.
dialogID = 1
componentID = 2
columnIndex = 1

ok, toolTipPrimaryText, toolTipSubText = vs.GetLBColumnHeaderToolTip(dialogID, componentID, columnIndex)
vs.Message('GetLBColumnHeaderToolTip returned: ' + str((ok, toolTipPrimaryText, toolTipSubText)))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
