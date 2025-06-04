# GetLBItemMkrChoice

## Description
Gets the specified list browser item's marker.

```pascal
PROCEDURE GetLBItemMkrChoice(
				dialogID           : LONGINT;
				componentID        : LONGINT;
				itemIndex          : INTEGER;
				subItemIndex       : INTEGER;
				VAR style          : LONGINT;
				VAR angle          : INTEGER;
				VAR size           : REAL;
				VAR width          : REAL;
				VAR thicknessBasis : INTEGER;
				VAR thickness      : REAL);
```

```python
def vs.GetLBItemMkrChoice(dialogID, componentID, itemIndex, subItemIndex):
    return (BOOLEAN, style, angle, size, width, thicknessBasis, thickness)
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
