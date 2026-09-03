# DeleteLBColumn

## Description
Deletes a column from the specified list browser control.

```pascal
FUNCTION DeleteLBColumn(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER): BOOLEAN;
```

```python
def vs.DeleteLBColumn(dialogID, componentID, columnIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|index of the column to be deleted|

## Examples
```pascal
resultOK := DeleteLBColumn(1, 2, 3);
```
```python
import vs

# Deletes a column from the specified list browser control.
dialogID = 1
componentID = 2
columnIndex = 1

ok = vs.DeleteLBColumn(dialogID, componentID, columnIndex)
if ok:
    vs.Message('DeleteLBColumn succeeded')
else:
    vs.Message('DeleteLBColumn failed')
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
