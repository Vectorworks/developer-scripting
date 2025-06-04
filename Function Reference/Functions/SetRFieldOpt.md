# SetRFieldOpt

## Description
Set options for a record field.

```pascal
PROCEDURE SetRFieldOpt(
				h            : HANDLE;
				record       : STRING;
				field        : STRING;
				isEmpty      : BOOLEAN;
				isDataLinked : BOOLEAN);
```

```python
def vs.SetRFieldOpt(h, record, field, isEmpty, isDataLinked):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to a object with an attached record.|
|record|STRING|Name of record to be updated.|
|field|STRING|Name of field to be updated.|
|isEmpty|BOOLEAN|Option to set, specifying this field as empty data for the Data Manager.|
|isDataLinked|BOOLEAN|Option to set, specifying this field data linked for the Data Manager.|

## Examples
```python
SetRField(HandleToObject,'Part Info','Serial No.',False, False);
```

## See Also
VS Functions:
[GetRFieldOpt](GetRFieldOpt.md) 
| [GetRField](GetRField.md) 
| [SetRField](SetRField.md)

## Version
Availability: from Vectorworks 2021

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
