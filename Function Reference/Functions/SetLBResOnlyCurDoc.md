# SetLBResOnlyCurDoc

## Description
Sets the specified list browser item to only use the current document when using/displaying resources.

```pascal
PROCEDURE SetLBResOnlyCurDoc(
				dialogID       : LONGINT;
				componentID    : LONGINT;
				itemIndex      : INTEGER;
				subItemIndex   : INTEGER;
				onlyCurrentDoc : BOOLEAN);
```

```python
def vs.SetLBResOnlyCurDoc(dialogID, componentID, itemIndex, subItemIndex, onlyCurrentDoc):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the item index|
|subItemIndex|INTEGER|the column index|
|onlyCurrentDoc|BOOLEAN|specifies whether or not only the current document should be used|

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
