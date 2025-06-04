# SetComponentSize

## Description
Sets the width and height of the specified Layout Manager component in pixels. 
Remark: Works in the dialog's setup handler. Can be used with AdjustComponentPixelPos.

```pascal
FUNCTION SetComponentSize(
				nDialogID     : LONGINT;
				nComponentID  : LONGINT;
				nWidthPixels  : INTEGER;
				nHeightPixels : INTEGER): BOOLEAN;
```

```python
def vs.SetComponentSize(nDialogID, nComponentID, nWidthPixels, nHeightPixels):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|nDialogID|LONGINT|   |
|nComponentID|LONGINT|   |
|nWidthPixels|INTEGER|   |
|nHeightPixels|INTEGER|   |

## Version
Availability: from VectorWorks13.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
