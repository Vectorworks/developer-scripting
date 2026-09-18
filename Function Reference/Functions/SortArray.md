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

## Examples
```pascal
ALLOCATE classListN [1..ClassNum];
FOR i := 1 TO ClassNum DO
	classListN [i] := ClassList (i);
SortArray(classListN, ClassNum, 0);

ALLOCATE classNames [1..ClassNum];
FOR i := 1 TO ClassNum DO
	classNames [i] := ClassList (i);
SortArray (classNames, ClassNum, 0);

BEGIN
	SortArray(list, list_cnt, 0);
END;
```
```python
import vs

# Sorts a 1-dimension array into ascending order.
numtosort = 5
fieldnumber = 1

result = vs.SortArray(numtosort, fieldnumber)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Utility](../Categories/Utility.md)
