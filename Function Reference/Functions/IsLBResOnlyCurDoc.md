# IsLBResOnlyCurDoc

## Description
Returns whether the specified list browser item is set, or not, to only use the current document when using/displaying resources.

```pascal
FUNCTION IsLBResOnlyCurDoc(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				itemIndex    : INTEGER;
				subItemIndex : INTEGER): BOOLEAN;
```

```python
def vs.IsLBResOnlyCurDoc(dialogID, componentID, itemIndex, subItemIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|itemIndex|INTEGER|the item index|
|subItemIndex|INTEGER|the column index|

## Version
Availability: from Vectorworks 2022

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
