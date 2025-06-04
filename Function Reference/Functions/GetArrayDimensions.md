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

## Version
Availability: from VectorWorks9.0

## Category
* [Utility](../Categories/Utility.md)
