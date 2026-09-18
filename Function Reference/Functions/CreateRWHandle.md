# CreateRWHandle

## Description
Create a new RenderWorks options handle.

```pascal
PROCEDURE CreateRWHandle(VAR RWHandle : HANDLE);
```

```python
def vs.CreateRWHandle():
    return RWHandle
```

## Parameters
|Name|Type|Description|
|---|---|---|
|RWHandle|HANDLE|   |

## Examples
```pascal
CreateRWHandle(RWHandle);
```
```python
import vs

# Create a new RenderWorks options handle.
objHandle = vs.CreateRWHandle()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
