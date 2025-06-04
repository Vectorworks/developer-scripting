# GetRFieldOpt

## Description
Get the options for a record field.

```pascal
PROCEDURE GetRFieldOpt(
				h                   : HANDLE;
				record              : STRING;
				field               : STRING;
				VAR outIsEmpty      : BOOLEAN;
				VAR outIsDataLinked : BOOLEAN);
```

```python
def vs.GetRFieldOpt(h, record, field):
    return (outIsEmpty, outIsDataLinked)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|record|STRING|Name of record format.|
|field|STRING|Name of field to be queried.|
|outIsEmpty|BOOLEAN|Output the flag for empty value used by the Data Manager.|
|outIsDataLinked|BOOLEAN|Output the flag for data linked value used by the Data Manager.|

## See Also
VS Functions:
[SetRFieldOpt](SetRFieldOpt.md) 
| [GetRField](GetRField.md) 
| [SetRField](SetRField.md)

## Version
Availability: from Vectorworks 2021

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
