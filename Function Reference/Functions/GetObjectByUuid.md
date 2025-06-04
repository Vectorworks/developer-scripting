# GetObjectByUuid

## Description
Function GetObjectByUuid returns a handle to the object with the specified UUID. If the UUID is not valid, or if no object with that UUID exists, NIL is returned.

```pascal
FUNCTION GetObjectByUuid(UUID : STRING): HANDLE;
```

```python
def vs.GetObjectByUuid(UUID):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|UUID|STRING|Object UUID|

## See Also
VS Functions:
[GetObjectUuid](GetObjectUuid.md)

## Version
Availability: from Vectorworks 2018.4

## Category
* [Object Info](../Categories/Object%20Info.md)
