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

## Examples
```pascal
resultN := GetLBItemDisplayType(1, 2, 3);
```
```python
import vs

# Gets item display type for list items in specified column.
dialogID = 1
componentID = 2
columnIndex = 1

resultN = vs.GetLBItemDisplayType(dialogID, componentID, columnIndex)
vs.Message('GetLBItemDisplayType returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
