# GetNumLBColumnDataItems

## Description
Get the number of columnDataItems.

```pascal
FUNCTION GetNumLBColumnDataItems(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER): INTEGER;
```

```python
def vs.GetNumLBColumnDataItems(dialogID, componentID, columnIndex):
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
resultN := GetNumLBColumnDataItems(1, 2, 3);
```
```python
import vs

# Get the number of columnDataItems.
dialogID = 1
componentID = 2
columnIndex = 1

count = vs.GetNumLBColumnDataItems(dialogID, componentID, columnIndex)
vs.Message('GetNumLBColumnDataItems returned: ' + str(count))
```

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
