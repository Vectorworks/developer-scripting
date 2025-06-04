# SetLBReadOnly

## Description
Sets the list browser's read-only state.

```pascal
PROCEDURE SetLBReadOnly(
				dialogID    : LONGINT;
				componentID : LONGINT;
				readOnly    : BOOLEAN);
```

```python
def vs.SetLBReadOnly(dialogID, componentID, readOnly):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|readOnly|BOOLEAN|the read-only state|

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
