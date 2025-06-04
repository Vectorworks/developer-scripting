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

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
