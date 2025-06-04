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

## Version
Availability: from Vectorworks 2015

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
