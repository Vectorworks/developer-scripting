# TBB_OpenTBBSelDlg

## Description
Open Title Block Border Selection Dialog

```pascal
PROCEDURE TBB_OpenTBBSelDlg(
				VAR StyleName : STRING;
				VAR SheetSize : STRING;
				VAR TBWidth   : REAL;
				VAR TBHeight  : REAL);
```

```python
def vs.TBB_OpenTBBSelDlg(StyleName, SheetSize, TBWidth, TBHeight):
    return (StyleName, SheetSize, TBWidth, TBHeight)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|StyleName|STRING|   |
|SheetSize|STRING|   |
|TBWidth|REAL|   |
|TBHeight|REAL|   |

## Examples
```pascal
	GetBooleanItem(dlogID, kTitleBlockBorderGroupBox, gUseTBB);
	EnableItem(dlogID, kTitleBlockPopup, gUseTBB  AND gDrawBorderNow);
END;
kTitleBlockBtn: BEGIN
	TBB_OpenTBBSelDlg(styleName, sheetSize, tbWidth, tbHeight);
END;

20: BEGIN
	TBB_OpenTBBSelDlg(gTitleBlockType, gBorderType, gTBWidth, gTBHeight);
END;
```
```python
import vs

# Open Title Block Border Selection Dialog.
StyleName = 'Example'
SheetSize = 'Example'
TBWidth = 2.0
TBHeight = 2.0

StyleName, SheetSize, TBWidth, TBHeight = vs.TBB_OpenTBBSelDlg(StyleName, SheetSize, TBWidth, TBHeight)
vs.Message('TBB_OpenTBBSelDlg returned: ' + str((StyleName, SheetSize, TBWidth, TBHeight)))
```

## Version
Availability: from Vectorworks 2019

## Category
* [Utility](../Categories/Utility.md)
