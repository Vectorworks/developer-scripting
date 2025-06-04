# LNewObj

## Description
Returns a handle to the last object created by a VectorScript function call during the current script execution.

```pascal
FUNCTION LNewObj : HANDLE;
```

```python
def vs.LNewObj():
    return HANDLE
```

## Remarks
[As of 8.0.0b10]

If the object has been deleted since it was created, this function returns NIL. It is recommended that you call LNewObj immediately after the function or procedure which created the object to avoid problems.

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
