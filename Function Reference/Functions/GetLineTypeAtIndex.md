# GetLineTypeAtIndex

## Description
Get the line type at the specified index in the line style control.

```pascal
PROCEDURE GetLineTypeAtIndex(
				dialogID     : LONGINT;
				itemID       : LONGINT;
				index        : INTEGER;
				VAR lineType : LONGINT);
```

```python
def vs.GetLineTypeAtIndex(dialogID, itemID, index):
    return lineType
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index of the line style control.|
|index|INTEGER|The choice index.|
|lineType|LONGINT|The internal index (reference number) of the line type.|

## Examples
```pascal
GetLineTypeAtIndex(1, 2, 3, 10);
```
```python
import vs

# Get the line type at the specified index in the line style control.
dialogID = 1
itemID = 2
index = 1

result = vs.GetLineTypeAtIndex(dialogID, itemID, index)
```

## Version
Availability: from Vectorworks 2015

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
