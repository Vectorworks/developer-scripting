# SetLBItemUsingColumnDataItem

## Description
Sets list item data with specified column data item.

```pascal
FUNCTION SetLBItemUsingColumnDataItem(
				dialogID            : LONGINT;
				componentID         : LONGINT;
				itemIndex           : INTEGER;
				subItemIndex        : INTEGER;
				columnDataItemIndex : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemUsingColumnDataItem(dialogID, componentID, itemIndex, subItemIndex, columnDataItemIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|columnDataItemIndex|INTEGER|the column data item with which to set list item data|

## Remarks
([[User:CBM-c-|_c_]], 2015.04.06): this crashes VW 2013 if the cell doesn't have any column data items. Check for the presence of data items in the chosen column using [GetNumLBColumnDataItems](GetNumLBColumnDataItems.md) in order to prevent accidentally using it on cells with no column data items:
<code lang="vs">
IF GetNumLBColumnDataItems(dialogID, listBrowserID, columnIndex) > 0 THEN BEGIN
   IF SetLBItemUsingColumnDataItem(dialogID, listBrowserID, rowIndex, columnIndex, columnDataItemIndex) THEN BEGIN
      { ... }
   END;
END;
</code>

## Version
Availability: from VectorWorks 11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
