# SetLBItemPatternIndex

## Description
Sets the specified list browser item's pattern index.

```pascal
FUNCTION SetLBItemPatternIndex(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER;
				patIndex     : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemPatternIndex(dialogID, componentID, itemIndex, subItemIndex, patIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|patIndex|INTEGER|The pattern index of this item. Value from [1..71] see [Sciprt Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#fill-patterns).|

## Examples
#### VectorScript ####
```pascal
SetupDialogC: BEGIN
  tmp := InsertLBColumn( dialog, kListBrowser, 0, 'one', 60 );
  tmp := InsertLBColumn( dialog, kListBrowser, 1, 'two', 60 );
  tmp := InsertLBItem( dialog, kListBrowser, 0, 'pat' );

  boo := SetLBControlType( dialog, kListBrowser, 1, 5 );
  boo := SetLBItemDisplayType( dialog, kListBrowser, 1, 1 );

  boo := SetLBColumnOwnerDrawnType( dialog, kListBrowser, 0, 1, 3 );
  boo := SetLBItemPatternIndex( dialog, kListBrowser, 0, 1, 9 );
  boo := SetLBItemFillForeColor( dialog, kListBrowser, 0, 1,   0, 0, 0 );
  boo := SetLBItemFillBackColor( dialog, kListBrowser, 0, 1,   255, 255, 255 );
END;
```
#### Python ####
```python

```

## See Also
[GetLBItemPatternIndex](GetLBItemPatternIndex.md) | [SetLBItemFillForeColor](SetLBItemFillForeColor.md) | [SetLBItemFillBackColor](SetLBItemFillBackColor.md)

[SetLBControlType](SetLBControlType.md) | [SetLBItemDisplayType](SetLBItemDisplayType.md) | [SetLBColumnOwnerDrawnType](SetLBColumnOwnerDrawnType.md) | [SetLBItemPatternIndex](SetLBItemPatternIndex.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
