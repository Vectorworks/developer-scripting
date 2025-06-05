# SetEditReal

## Description
Sets the numeric value of the specified REAL numeric edit field control.

**Table - Field Types for EditReal Fields**

| Index | Field Value   |
|-------|--------------|
| 1     | REAL value   |
| 2     | Angular value|
| 3     | Dimension    |
| 4     | X coordinate |
| 5     | Y coordinate |

```pascal
PROCEDURE SetEditReal(
				dialogID     : LONGINT;
				itemID       : LONGINT;
				editRealType : LONGINT;
				value        : REAL);
```

```python
def vs.SetEditReal(dialogID, itemID, editRealType, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index of the control item.|
|editRealType|LONGINT|The type of REAL value displayed in the field.|
|value|REAL|The new value for the field.|

## Remarks
Note that dimension reals do not accept negative numbers. If your field might contain negatives, and you still want the units mark to show, use x or y coordinate reals.

## Version
Availability: from VectorWorks 9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
