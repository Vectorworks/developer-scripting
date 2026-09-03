# CreatePullDownMenuGroupBox

## Description
Creates a Layout Manager pull down menu group box.

```pascal
PROCEDURE CreatePullDownMenuGroupBox(
				liDialogID     : LONGINT;
				liComponentID  : LONGINT;
				iPullDownWidth : INTEGER;
				strLabel       : STRING;
				bHasFrame      : BOOLEAN);
```

```python
def vs.CreatePullDownMenuGroupBox(liDialogID, liComponentID, iPullDownWidth, strLabel, bHasFrame):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|liDialogID|LONGINT|   |
|liComponentID|LONGINT|   |
|iPullDownWidth|INTEGER|   |
|strLabel|STRING|   |
|bHasFrame|BOOLEAN|   |

## Examples
```pascal
CreateEditReal( dialog, kEdBxBmpAWeight, 1, 50, 5 );
CreatePullDownMenuGroupBox( dialog, kBmpAExtBarChcePUGrp, 14, GetStr(kBmpAExtBarChcePUGrp), TRUE );
CreateStaticText( dialog, kBmpAExtBarSpacer, ' ', -1 );
CreateStaticText( dialog, kBmpAExtBarLengthLab, GetStr(kBmpAExtBarLengthLab), -1 );
CreateEditReal( dialog, kBmpAExtBarLengthBx, 3, 48", 10 );
CreateStaticText( dialog, kBmpAExtBarHeightLab, GetStr(kBmpAExtBarHeightLab), -1 );
```
```python
import vs

# Creates a Layout Manager pull down menu group box.
liDialogID = 1
liComponentID = 2
iPullDownWidth = 3
strLabel = 'Example text'
bHasFrame = True

vs.CreatePullDownMenuGroupBox(liDialogID, liComponentID, iPullDownWidth, strLabel, bHasFrame)
newObj = vs.LNewObj()  # handle to the newly created object
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
