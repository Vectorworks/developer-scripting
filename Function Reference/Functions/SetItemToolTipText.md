# SetItemToolTipText

## Description
Sets the tooltip text for list browsers, list boxes, edit controls, pull down menus, and enhanced static text.  Parameters nIndex and nSubIndex are used for list browsers and list boxes only.

```pascal
PROCEDURE SetItemToolTipText(
				nDialogID     : LONGINT;
				nComponentID  : LONGINT;
				strToolTip    : STRING;
				strSubToolTip : STRING;
				nIndex        : INTEGER;
				nSubIndex     : INTEGER);
```

```python
def vs.SetItemToolTipText(nDialogID, nComponentID, strToolTip, strSubToolTip, nIndex, nSubIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|strToolTip|STRING|   |
|strSubToolTip|STRING|   |
|nIndex|INTEGER|   |
|nSubIndex|INTEGER|   |

## Examples
```pascal
{Special Items}
FOR i:=kFirstSpecItemStr TO kFirstSpecItemStr+kNumSpecialItems-1 DO BEGIN
	tempInt:=InsertLBItem(dialogIDSetup, kBrowserOther, GetNumLBItems(dialogIDSetup, kBrowserOther), GetStr2(i));
	SetItemToolTipText(dialogIDSetup, kBrowserOther, GetStr2(i), GetStr2(i+kSpecTipOffset), tempInt, 0);
END;
```
```python
import vs

# Sets the tooltip text for list browsers, list boxes, edit controls, pull
# down menus, and enhanced static text.
nDialogID = 1
nComponentID = 2
strToolTip = 'Example'
strSubToolTip = 'Example'
nIndex = 1
nSubIndex = 1

vs.SetItemToolTipText(nDialogID, nComponentID, strToolTip, strSubToolTip, nIndex, nSubIndex)
```

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
