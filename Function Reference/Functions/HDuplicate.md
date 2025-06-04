# HDuplicate

## Description
Duplicates and moves an object by the offsets specified.

```pascal
FUNCTION HDuplicate(
				objectHandle : HANDLE;
				x            : REAL;
				y            : REAL): HANDLE;
```

```python
def vs.HDuplicate(objectHandle, x, y):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the object to duplicate|
|x|REAL|X-coordinate of distance object should be shifted from original location|
|y|REAL|Y-coordinate of distance object should be shifted from original location|

## Version
Availability: from VectorWorks10.0

## Category
* [Object Editing](../Categories/Object%20Editing.md)
