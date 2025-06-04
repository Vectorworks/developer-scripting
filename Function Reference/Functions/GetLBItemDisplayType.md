# GetLBItemDisplayType

## Description
Gets item display type for list items in specified column.

```pascal
FUNCTION GetLBItemDisplayType(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER): INTEGER;
```

```python
def vs.GetLBItemDisplayType(dialogID, componentID, columnIndex):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
