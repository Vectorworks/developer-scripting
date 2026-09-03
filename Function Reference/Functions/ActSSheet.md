# ActSSheet

## Description
Function ActSSheet returns the handle to the currently active worksheet.

```pascal
FUNCTION ActSSheet : HANDLE;
```

```python
def vs.ActSSheet():
    return HANDLE
```

## Remarks
OBSOLETE for Version 9: see new [GetTopVisibleWS](GetTopVisibleWS.md).

## Examples
```pascal
resultH := ActSSheet;
```
```python
import vs

# Function ActSSheet returns the handle to the currently active worksheet.
objHandle = vs.ActSSheet()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[GetTopVisibleWS](GetTopVisibleWS.md)

## Version
ActSSheet is obsolete as of VectorWorks 9.0

Availability: from All Versions

## Category
* [Worksheets](../Categories/Worksheets.md)
