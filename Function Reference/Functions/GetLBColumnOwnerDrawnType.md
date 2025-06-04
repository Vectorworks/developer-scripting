# GetLBColumnOwnerDrawnType

## Description
Gets the list browser column's owner drawn type.

```pascal
FUNCTION GetLBColumnOwnerDrawnType(
				dialogID           : LONGINT;
				componentID        : LONGINT;
				itemIndex          : INTEGER;
				subItemIndex       : INTEGER;
				VAR ownerDrawnType : INTEGER): BOOLEAN;
```

```python
def vs.GetLBColumnOwnerDrawnType(dialogID, componentID, itemIndex, subItemIndex):
    return (BOOLEAN, ownerDrawnType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|ownerDrawnType|INTEGER|None - 0|Solid rect - 1|Dual solid rect - 2|Pattern rect - 3|Dual pattern rect - 4|Gradient or image - 5|Blank - 6|Text - 7|Dashed line - 8|

## Remarks
([[User:Orso.b.schmid|Orso]], 2011 Oct. 08): This routine is non functional (tested from VW12 up to VW16): while it doesn't fail, it always sets "ownerDrawnType" to "0".

## Version
Availability: from VectorWorks 12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
