# SetRecord

## Description
Assigns an instance of an existing record format to the referenced object .

```pascal
PROCEDURE SetRecord(
				h      : HANDLE;
				record : STRING);
```

```python
def vs.SetRecord(h, record):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|record|STRING|Name of record to assign to object.|

## Examples
==== VectorScript ====
```pascal
SetRecord(HandleToObject,'Part Info');
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
