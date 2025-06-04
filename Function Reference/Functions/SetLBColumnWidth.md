# SetLBColumnWidth

## Description
Sets the width of the specified range of columns of the specified list browser control.

```pascal
FUNCTION SetLBColumnWidth(
				dialogID    : LONGINT;
				componentID : LONGINT;
				fromColumn  : INTEGER;
				toColumn    : INTEGER;
				width       : INTEGER): BOOLEAN;
```

```python
def vs.SetLBColumnWidth(dialogID, componentID, fromColumn, toColumn, width):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|fromColumn|INTEGER|first column to be changed|
|toColumn|INTEGER|last column to be changed|
|width|INTEGER|the width of the column in pixels|

## Remarks
On the Mac a List Browser column width of '0' will crash the application or make the dialog window un-exitable (force-quit needed). The same occurs if a user is resetting manually the column width to zero.

This known, the column width zero must be prevented programmatically for safety (VW 12.5-13).

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
