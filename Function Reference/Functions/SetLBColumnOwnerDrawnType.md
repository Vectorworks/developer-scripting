# SetLBColumnOwnerDrawnType

## Description
Sets the list browser column's owner drawn type.

```pascal
FUNCTION SetLBColumnOwnerDrawnType(
				dialogID       : LONGINT;
				componentID    : LONGINT;
				itemIndex      : INTEGER;
				subItemIndex   : INTEGER;
				ownerDrawnType : INTEGER): BOOLEAN;
```

```python
def vs.SetLBColumnOwnerDrawnType(dialogID, componentID, itemIndex, subItemIndex, ownerDrawnType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|ownerDrawnType|INTEGER|None - 0, Solid rect - 1, Dual solid rect - 2, Pattern rect - 3, Dual pattern rect - 4, Gradient or image - 5, Blank - 6, Text - 7, Dashed line - 8|

## Remarks
([[User:CBM-c-|_c_]], 2015.12.19): 
Pattern and pattern rects are supported starting with VW 15 (2010). Use [SetLBItemPatternIndex](SetLBItemPatternIndex.md) to choose the Pattern.

([[User:CBM-c-|_c_]], 2007.05.16): 
Pattern and pattern rect are not quite supported under VW 12.5 and 12.5.1. Setting a LB cell to this type will only load the artifact of a pattern. The image loaded is by default random and stretches on Mac (not on PC). A pattern shouldn't stretch according to the width of the LB cell, should be bound to the screen resolution.

There is to my knowledge no way to control the pattern loaded.
A corresponding function for setting or retriving the pattern index is still missing in the currently published VS version. In the SDK there are [[SDK:GS_SetListBrowserItemPatternIndex]] and [[SDK:GS_GetListBrowserItemPatternIndex]].

## Version
Availability: from VectorWorks 12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
