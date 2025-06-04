# NumRecords

## Description
Returns the number of records attached to the referenced object.

```pascal
FUNCTION NumRecords(h : HANDLE): INTEGER;
```

```python
def vs.NumRecords(h):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Examples
#### VectorScript ####
```pascal
numAttached:=NumRecords(HandleToObject);
```
#### Python ####
```python
numAttached = vs.NumRecords(HandleToObject)
```

## Version
Availability: from All Versions

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
