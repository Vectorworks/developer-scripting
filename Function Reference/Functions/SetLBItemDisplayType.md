# SetLBItemDisplayType

## Description
Sets item display type for list items in specified column.

```pascal
FUNCTION SetLBItemDisplayType(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER;
				displayType : INTEGER): BOOLEAN;
```

```python
def vs.SetLBItemDisplayType(dialogID, componentID, columnIndex, displayType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|
|displayType|INTEGER|the display type to be set (0: Text Only, 1: Icon Only, 3: Text and Icon)|

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
