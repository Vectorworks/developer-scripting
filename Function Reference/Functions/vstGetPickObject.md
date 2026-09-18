# vstGetPickObject

## Description
Looks like this is the same as [PickObject](PickObject.md), except that it works inside an event-enabled tool loop.

```pascal
FUNCTION vstGetPickObject() :HANDLE;
```

```python
def vs.vstGetPickObject():
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
||   |   |

## Examples
```pascal
resultH := vstGetPickObject;
```
```python
import vs

# Looks like this is the same as PickObject, except that it works inside an
# event-enabled tool loop.
objHandle = vs.vstGetPickObject()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
