# GetLBColumnHeaderJust

## Description
Retrieves the specified column header's justification.

```pascal
FUNCTION GetLBColumnHeaderJust(
				dialogID          : LONGINT;
				componentID       : LONGINT;
				columnIndex       : INTEGER;
				VAR justification : INTEGER): BOOLEAN;
```

```python
def vs.GetLBColumnHeaderJust(dialogID, componentID, columnIndex):
    return (BOOLEAN, justification)
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
resultOK := GetLBColumnHeaderJust(1, 2, 3, 10);
```
```python
import vs

# Retrieves the specified column header's justification.
dialogID = 1
componentID = 2
columnIndex = 1

ok, justification = vs.GetLBColumnHeaderJust(dialogID, componentID, columnIndex)
vs.Message('GetLBColumnHeaderJust returned: ' + str((ok, justification)))
```

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
