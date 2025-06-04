# SetLBItemTextJust

## Description
Sets the text alignment for the specified list browser item.

```pascal
FUNCTION SetLBItemTextJust(
				dialogID      : LONGINT;
				componentID   : LONGINT;
				itemIndex     : INTEGER;
				subItemIndex  : INTEGER;
				justification : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemTextJust(dialogID, componentID, itemIndex, subItemIndex, justification):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the row index|
|subItemIndex|INTEGER|the column index|
|justification|INTEGER|Left - 1|Center - 2|Right - 3|

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
