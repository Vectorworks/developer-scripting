# SetLBColumnImage

## Description
Draws an icon instead of text on a list browser header column.  Use with AddListBrowserImage.

```pascal
FUNCTION SetLBColumnImage(
				nDialogID    : LONGINT;
				nComponentID : LONGINT;
				nColumnIndex : INTEGER;
				nImageIndex  : INTEGER): BOOLEAN;
```

```python
def vs.SetLBColumnImage(nDialogID, nComponentID, nColumnIndex, nImageIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nColumnIndex|INTEGER|   |
|nImageIndex|INTEGER|   |

## Examples
```pascal
resultOK := SetLBColumnImage(1, 2, 3, 10);
```
```python
import vs

# Draws an icon instead of text on a list browser header column.
nDialogID = 1
nComponentID = 2
nColumnIndex = 1
nImageIndex = 1

ok = vs.SetLBColumnImage(nDialogID, nComponentID, nColumnIndex, nImageIndex)
if ok:
    vs.Message('SetLBColumnImage succeeded')
else:
    vs.Message('SetLBColumnImage failed')
```

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
