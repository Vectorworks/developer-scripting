# GetArrayDimensions

## Description
Returns the dimensions of the specified array.

```pascal
PROCEDURE GetArrayDimensions(
				arrayname       : ARRAY;
				VAR rowStart    : INTEGER;
				VAR rowEnd      : INTEGER;
				VAR columnStart : INTEGER;
				VAR columnEnd   : INTEGER);
```

```python
def vs.GetArrayDimensions(arrayname):
    return (rowStart, rowEnd, columnStart, columnEnd)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|arrayname|ARRAY|Name of array.|
|rowStart|INTEGER|Start row value.|
|rowEnd|INTEGER|End row value.|
|columnStart|INTEGER|Start column value.|
|columnEnd|INTEGER|End column value.|

## Remarks
Works for both regular and dynamic arrays. Returns 0 for column dimensions of the array is 1-dimensional.

## Examples
```pascal
		localCnt := glToBeDeletedSize + 2;
END;
if ( localCnt < glToBeDeletedSize + 2 ) then BEGIN
	glToBeDeletedSize := glToBeDeletedSize + 1;
	GetArrayDimensions( gm_HToBeDeleted, rowStart, rowEnd, columnStart, columnEnd );
	if ( rowEnd < glToBeDeletedSize ) then ALLOCATE gm_HToBeDeleted[1..rowEnd+kHToBeDeletedResize];
	gm_HToBeDeleted[glToBeDeletedSize] := delh;
END;

BEGIN
GetArrayDimensions(VPData, RowStart,RowEnd,ColStart,ColEnd);
NumVPs := NumVPs+1;
IF RowEnd < NumVPs THEN
		ALLOCATE VPData [1..RowEnd+50];
VPData[NumVPs].VPName := GetName(h);

BEGIN
GetArrayDimensions(ItemNumArray,rowStart,rowEnd,columnStart,columnEnd);
IF CurrentNumber > rowEnd THEN
	BEGIN
	ALLOCATE ItemNumArray[0..CurrentNumber];
	For I := rowEnd+1 to CurrentNumber DO
```
```python
import vs

# Returns the dimensions of the specified array.
arrayname = 'Example'

rowStart, rowEnd, columnStart, columnEnd = vs.GetArrayDimensions(arrayname)
vs.Message('GetArrayDimensions returned: ' + str((rowStart, rowEnd, columnStart, columnEnd)))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Utility](../Categories/Utility.md)
