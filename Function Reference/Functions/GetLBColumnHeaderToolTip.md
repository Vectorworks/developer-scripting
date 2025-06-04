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

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
