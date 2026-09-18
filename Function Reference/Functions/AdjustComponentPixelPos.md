# AdjustComponentPixelPos

## Description
Adjust the position offset of the specified Layout Manager component in pixels.
Remark: Works in the dialog's setup handler. Can be used with SetComponentSize.

```pascal
FUNCTION AdjustComponentPixelPos(
				nDialogID         : LONGINT;
				nComponentID      : LONGINT;
				nHorizontalPixels : INTEGER;
				nVerticalPixels   : INTEGER): BOOLEAN;
```

```python
def vs.AdjustComponentPixelPos(nDialogID, nComponentID, nHorizontalPixels, nVerticalPixels):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nHorizontalPixels|INTEGER|   |
|nVerticalPixels|INTEGER|   |

## Examples
```pascal
resultOK := AdjustComponentPixelPos(1, 2, 3, 10);
```
```python
import vs

# Adjust the position offset of the specified Layout Manager component in pixels.
nDialogID = 1
nComponentID = 2
nHorizontalPixels = 3
nVerticalPixels = 10

ok = vs.AdjustComponentPixelPos(nDialogID, nComponentID, nHorizontalPixels, nVerticalPixels)
if ok:
    vs.Message('AdjustComponentPixelPos succeeded')
else:
    vs.Message('AdjustComponentPixelPos failed')
```

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
