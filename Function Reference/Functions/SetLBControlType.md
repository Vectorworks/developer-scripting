# SetLBControlType

## Description
Sets control type for column.

```pascal
FUNCTION SetLBControlType(
				dialogID    : LONGINT;
				componentID : LONGINT;
				columnIndex : INTEGER;
				controlType : INTEGER): BOOLEAN;
```

```python
def vs.SetLBControlType(dialogID, componentID, columnIndex, controlType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|columnIndex|INTEGER|the index of the column|
|controlType|INTEGER|the control type to be set (1: Static, 2: Radio, 3: Multi State, 4: Single Instance Icon [See Organization Dialog active element column], 5: Static Icon, 6: Number, 7: Multiple Icons)|

## Version
Availability: from VectorWorks11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
