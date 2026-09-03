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
#### VectorScript ####
```pascal
totalFields:=NumFields(HandleToRecord);
```
#### Python ####
```python

```

```pascal
BEGIN
	nFields := NumFields (recordH);
	ALLOCATE fieldN [1..nFields];

BEGIN
	gNFields := NumFields (recordH);
	IF gNFields > gMaxFields THEN
	BEGIN
		ALLOCATE fieldN [1..gNFields];
		gMaxFields := gNFields;

for i := 1 to NumFields(recHandle) do BEGIN
	str := GetFldName(recHandle, i); {*****}
	PopSub2;
END; {*****}
```
```python
result = vs.NumFields(h)
```
See also in tutorials: [Plug-in with widgets, basic example (Python)](../../Common/Tasks/Parametrics/Plug-in%20with%20widget%20basic%20example.md)

## Version
Availability: from All Versions

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
