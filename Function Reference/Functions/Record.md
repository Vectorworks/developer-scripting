# Record

## Description
Replaces an existing record with a new version of the same record. Parameter s specifies the record to be updated.

```pascal
PROCEDURE Record(
				h : HANDLE;
				s : STRING);
```

```python
def vs.Record(h, s):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|s|STRING|Name of record to be updated.|

## Remarks
Delete any existing record named &quot;s&quot; on &quot;h&quot;, Create new record for format named 's', attach to &quot;h&quot;.

## Examples
==== VectorScript ====
```pascal
Record(handleToObj,'Vendor Information');
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
