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

## Examples
```pascal
SetLBItemMkrChoice(1, 2, 3, 10, 5, 1, 1.0, 2.0, 2, 0.5);
```
```python
import vs

# Sets the specified list browser item's marker.
dialogID = 1
componentID = 2
itemIndex = 1
subItemIndex = 1
style = 0
angle = 3
size = 1.0
width = 2.0
thicknessBasis = 10
thickness = 0.1

ok = vs.SetLBItemMkrChoice(dialogID, componentID, itemIndex, subItemIndex, style, angle, size, width, thicknessBasis, thickness)
if ok:
    vs.Message('SetLBItemMkrChoice succeeded')
else:
    vs.Message('SetLBItemMkrChoice failed')
```

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
