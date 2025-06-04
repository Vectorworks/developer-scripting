# UseDefaultFileErrorHandling

## Description
Enables or disables file I/O alert dialogs.

Use this function with GetLastFileErr() to implement custom error handling for file operations.

```pascal
PROCEDURE UseDefaultFileErrorHandling(enable : BOOLEAN);
```

```python
def vs.UseDefaultFileErrorHandling(enable):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|enable|BOOLEAN|Status of file error dialog usage.|

## See Also
VS Functions:
[GetLastFileErr](GetLastFileErr.md)

## Version
Availability: from VectorWorks8.5

## Category
* [File I@O](../Categories/File%20IO.md)
