# GetEditReal

## Description
Returns the numeric value from the specified REAL numeric edit field control.

```pascal
FUNCTION GetEditReal(
				dialogID     : LONGINT;
				itemID       : LONGINT;
				editRealType : LONGINT;
				VAR value    : REAL): BOOLEAN;
```

```python
def vs.GetEditReal(dialogID, itemID, editRealType):
    return (BOOLEAN, value)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The index of the dialog layout containing the control.|
|itemID|LONGINT|The index of the control item.|
|editRealType|LONGINT|The type of REAL value being returned.|
|value|REAL|The value contained in the field.|

## Remarks
does math, handles units, returns false for any error in conversion. For an explanation of editRealType, see the CreateEditReal call

## Examples
==== VectorScript ====
```pascal
PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);

PROCEDURE InvalidValue(controlID :INTEGER);
BEGIN
item := -1;
SelField(controlID);
SysBeep;
END;

BEGIN
CASE item OF
SetupDialogC: SetEditReal(dialogID, 11, 3, elevation);
1: IF NOT(GetEditReal(dialogID, 11, 3, elevation)) 
THEN InvalidValue(11);
END;
END;
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
