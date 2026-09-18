# CreateHLHandle

## Description
Create a new Hidden Line Rendering options handle.

```pascal
PROCEDURE CreateHLHandle(VAR HLOptionsHandle : HANDLE);
```

```python
def vs.CreateHLHandle():
    return HLOptionsHandle
```

## Parameters
|Name|Type|Description|
|---|---|---|
|HLOptionsHandle|HANDLE|   |

## Examples
```pascal
CreateHLHandle(HLOptionsHandle);
```
```python
import vs

# Create a new Hidden Line Rendering options handle.
objHandle = vs.CreateHLHandle()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
