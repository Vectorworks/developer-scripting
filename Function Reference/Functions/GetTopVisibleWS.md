# GetTopVisibleWS

## Description
Returns a handle to topmost visible worksheet.

```pascal
FUNCTION GetTopVisibleWS : HANDLE;
```

```python
def vs.GetTopVisibleWS():
    return HANDLE
```

## Examples
```pascal
resultH := GetTopVisibleWS;
```
```python
import vs

# Returns a handle to topmost visible worksheet.
objHandle = vs.GetTopVisibleWS()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
