# CreateSheetLayerPullDownMenu

## Description
Creates a Layout Manager sheet layer pull down menu control.

```pascal
PROCEDURE CreateSheetLayerPullDownMenu(
				nDialogID     : LONGINT;
				nComponentID  : LONGINT;
				nWidthInChars : INTEGER);
```

```python
def vs.CreateSheetLayerPullDownMenu(nDialogID, nComponentID, nWidthInChars):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nWidthInChars|INTEGER|   |

## Examples
```pascal
CreateSheetLayerPullDownMenu(1, 2, 3);
```
```python
import vs

# Creates a Layout Manager sheet layer pull down menu control.
nDialogID = 1
nComponentID = 2
nWidthInChars = 3

vs.CreateSheetLayerPullDownMenu(nDialogID, nComponentID, nWidthInChars)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
