# GetRecord

## Description
Returns the handle to a specified record attached the referenced object.

```pascal
FUNCTION GetRecord(
				h   : HANDLE;
				cnt : INTEGER): HANDLE;
```

```python
def vs.GetRecord(h, cnt):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|cnt|INTEGER|Index of attached record (in a range of 1 -  n).|

## Remarks
*\_c\_*, 2015.02.24:
Please note that since the introduction of ifc data, the usual praxis of fetching plug-in records using GetRecord(h, NumRecords(h)) can bring you perhaps unexpectedly the ifc record. Use [GetParametricRecord](GetParametricRecord.md) instead, introduced from VW 2011.

## Examples
#### VectorScript ####
```pascal
handleToRecord := GetRecord(handleToObject,3);
```
#### Python ####
```python
handleToRecord = vs.GetRecord(handleToObject,3)
```

## Version
Availability: from All Versions

## Category
* [Database @ Record](../Categories/Database%20-%20Record.md)
