# GetLBEditDisplayType

## Description
Gets edit display type for list items in specified column.

```pascal
FUNCTION GetLBEditDisplayType(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER): INTEGER;
```

```python
def vs.GetLBEditDisplayType(dialogID, componentID, columnIndex):
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
