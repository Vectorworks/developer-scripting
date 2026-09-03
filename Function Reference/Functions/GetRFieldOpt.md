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

## Examples
```pascal
GetRFieldOpt(h, 'MyRecord', 'MyRecord', TRUE, FALSE);
```
```python
import vs

# Get the options for a record field.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
record = 'MyRecord'
field = 'MyField'

outIsEmpty, outIsDataLinked = vs.GetRFieldOpt(h, record, field)
vs.Message('GetRFieldOpt returned: ' + str((outIsEmpty, outIsDataLinked)))
```

## See Also
VS Functions:
[SetRFieldOpt](SetRFieldOpt.md) 
| [GetRField](GetRField.md) 
| [SetRField](SetRField.md)

## Version
Availability: from Vectorworks 2021

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
