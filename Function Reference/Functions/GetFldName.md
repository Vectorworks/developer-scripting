# GetFldName

## Description
Returns the name of the specified field in the referenced record.

```pascal
FUNCTION GetFldName(
				h     : HANDLE;
				index : INTEGER): STRING;
```

```python
def vs.GetFldName(h, index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to record.|
|index|INTEGER|Number of field whose name will be returned (in a range of 1-n).|

## Examples
#### VectorScript ####
```pascal
FName:=GetFldName(HandleToRecord,1);
```
#### Python ####
```python
FName = vs.GetFldName(HandleToRecord,1)
```

## Version
Availability: from All Versions

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
