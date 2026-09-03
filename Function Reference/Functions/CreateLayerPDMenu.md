# CreateLayerPDMenu

## Description
Creates a Layout Manager layer pull down menu control.

```pascal
PROCEDURE CreateLayerPDMenu(
				nDialogID           : LONGINT;
				nComponentID        : LONGINT;
				widthInStandardChar : INTEGER);
```

```python
def vs.CreateLayerPDMenu(nDialogID, nComponentID, widthInStandardChar):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|widthInStandardChar|INTEGER|The width of the displayed text in standard character count. See GetDlgCtrlWidthStdCh.|

## Examples
```pascal
CreateLayerPDMenu(1, 2, 3);
```
```python
import vs

# Creates a Layout Manager layer pull down menu control.
nDialogID = 1
nComponentID = 2
widthInStandardChar = 3

vs.CreateLayerPDMenu(nDialogID, nComponentID, widthInStandardChar)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from Vectorworks 2020

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
