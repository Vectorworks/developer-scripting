# GetFldFlag

## Description
Returns a number indicating the accuracy flag of a specified field in the referenced record.

```pascal
FUNCTION GetFldFlag(
				h : HANDLE;
				t : INTEGER): INTEGER;
```

```python
def vs.GetFldFlag(h, t):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to record.|
|t|INTEGER|Field index (range of 1 - n).|

## Examples
```python
fieldType:=GetFldFlag(recordHandle,3);
```

## Version
Availability: from Vectorworks 2016

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
