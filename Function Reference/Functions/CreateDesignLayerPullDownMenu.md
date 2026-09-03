# CreateDesignLayerPullDownMenu

## Description
Creates a Layout Manager design layer pull down menu control.

```pascal
PROCEDURE CreateDesignLayerPullDownMenu(
				nDialogID     : LONGINT;
				nComponentID  : LONGINT;
				nWidthInChars : INTEGER);
```

```python
def vs.CreateDesignLayerPullDownMenu(nDialogID, nComponentID, nWidthInChars):
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
CreateDesignLayerPullDownMenu(dialogID, ChooseLayerPop_ID, 40);
SetBelowItem( dialogID, ChooseLayerStaTex_ID, ChooseLayerPop_ID, 0, 0 );

BEGIN
	DialogID := CreateLayout(GetPlugInString(3000),TRUE,GetPlugInString(3001),GetPlugInString(3002));
	CreateStaticText(DialogID,4,GetPlugInString(3004),-1);
	CreateDesignLayerPullDownMenu (DialogID,5,25); {Layer name}
```
```python
import vs

# Creates a Layout Manager design layer pull down menu control.
nDialogID = 1
nComponentID = 2
nWidthInChars = 3

vs.CreateDesignLayerPullDownMenu(nDialogID, nComponentID, nWidthInChars)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
