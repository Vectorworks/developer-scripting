# SortArray

## Description
Sorts a 1-dimension array into ascending order. If the array contains handles to records, the array can be sorted by the specified field number index. If the array is an array of structures, the fieldnumber argument denotes the element in the structure on which to sort.

```pascal
PROCEDURE SortArray(
				VAR arraytosort : ARRAY;
				numtosort       : INTEGER;
				fieldnumber     : INTEGER);
```

```python
def vs.SortArray(numtosort, fieldnumber):
    return arraytosort
```

## Parameters
|Name|Type|Description|
|---|---|---|
|arraytosort|ARRAY|   |
|numtosort|INTEGER|   |
|fieldnumber|INTEGER|   |

## Remarks
[richn 1/21/00]

Sorts first numtosort elements of single-dimensional array  arraytosort into ascending order. If arraytosort is an array of records, it sorts on the fieldnumberth field of the record.

## Version
Availability: from VectorWorks9.0

## Category
* [Utility](../Categories/Utility.md)
