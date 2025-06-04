# GetEditInteger

## Description
Returns the numeric value from the specified INTEGER numeric edit field control.

```pascal
FUNCTION GetEditInteger(
				dialogID  : LONGINT;
				itemID    : LONGINT;
				VAR value : LONGINT): BOOLEAN;
```

```python
def vs.GetEditInteger(dialogID, itemID):
    return (BOOLEAN, value)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index of the control item.|
|value|LONGINT|The value contained in the field.|

## Remarks
does math, returns false for any error in conversion

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
