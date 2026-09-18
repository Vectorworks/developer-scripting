# vstGetToolObject

## Description
The installed [vstSetPtBehavior](vstSetPtBehavior.md) might create an object with tool complete. [vstGetToolObject](vstGetToolObject.md) returns this object

```pascal
FUNCTION vstGetToolObject() :HANDLE;
```

```python
def vs.vstGetToolObject():
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
||   |   |

## Examples
```pascal
resultH := vstGetToolObject;
```
```python
import vs

# The installed vstSetPtBehavior might create an object with tool complete.
objHandle = vs.vstGetToolObject()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
