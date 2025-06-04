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

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
