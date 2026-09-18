# GetNumLineTypeItems

## Description
Returns the number of line types in the line style control.

```pascal
FUNCTION GetNumLineTypeItems(
				dialogID : LONGINT;
				itemID   : LONGINT): INTEGER;
```

```python
def vs.GetNumLineTypeItems(dialogID, itemID):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index of the line style control.|

## Examples
```pascal
resultN := GetNumLineTypeItems(1, 2);
```
```python
import vs

# Returns the number of line types in the line style control.
dialogID = 1
itemID = 2

count = vs.GetNumLineTypeItems(dialogID, itemID)
vs.Message('GetNumLineTypeItems returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2015

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
