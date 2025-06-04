# SetLBSelection

## Description
Selects the specified range of items within a List Browser dialog control.

```pascal
FUNCTION SetLBSelection(
				dialogID       : LONGINT;
				componentID    : LONGINT;
				firstItemIndex : INTEGER;
				lastItemIndex  : INTEGER;
				select         : BOOLEAN): BOOLEAN;
```

```python
def vs.SetLBSelection(dialogID, componentID, firstItemIndex, lastItemIndex, select):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|firstItemIndex|INTEGER|the first row of the range to select|
|lastItemIndex|INTEGER|the last row of the range to select|
|select|BOOLEAN|select or deselect|

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
