# SetLBItemMkrChoice

## Description
Sets the specified list browser item's marker.

```pascal
PROCEDURE SetLBItemMkrChoice(
				dialogID       : LONGINT;
				componentID    : LONGINT;
				itemIndex      : INTEGER;
				subItemIndex   : INTEGER;
				style          : LONGINT;
				angle          : INTEGER;
				size           : REAL;
				width          : REAL;
				thicknessBasis : INTEGER;
				thickness      : REAL);
```

```python
def vs.SetLBItemMkrChoice(dialogID, componentID, itemIndex, subItemIndex, style, angle, size, width, thicknessBasis, thickness):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|style|LONGINT|the marker's style|
|angle|INTEGER|the marker's angle|
|size|REAL|the marker's size|
|width|REAL|the marker's width|
|thicknessBasis|INTEGER|the marker's thickness basis|
|thickness|REAL|the marker's thickness|

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
