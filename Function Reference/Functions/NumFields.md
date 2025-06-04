# NumFields

## Description
Returns the number of fields in the referenced record.

```pascal
FUNCTION NumFields(h : HANDLE): INTEGER;
```

```python
def vs.NumFields(h):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to record.|

## Examples
==== VectorScript ====
```pascal
totalFields:=NumFields(HandleToRecord);
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
