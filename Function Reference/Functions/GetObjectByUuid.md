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

## Examples
```pascal
{ now the Space Name can be anything, and we need to used the actual internal object UUID }
{ if the new 'Space1UUID' parameter exists and is valid, use it }
{ otherwise try to find the object using the value in 'Space1' as an object name  }
space1 := GetRField(objHand, objName, 'Space1UUID');
h1 := GetObjectByUuid(space1);
if (h1 = nil) then BEGIN
	space1 := GetRField(objHand, objName, 'Space1');
	h1 := GetObject(space1);
	uuid := GetObjectUuid(h1);
```
```python
import vs

# Function GetObjectByUuid returns a handle to the object with the specified
# UUID.
UUID = 'Example'

objHandle = vs.GetObjectByUuid(UUID)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[GetObjectUuid](GetObjectUuid.md)

## Version
Availability: from Vectorworks 2018.4

## Category
* [Object Info](../Categories/Object%20Info.md)
