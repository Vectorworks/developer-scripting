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

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
