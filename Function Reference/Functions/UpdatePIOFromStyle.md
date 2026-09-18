# UpdatePIOFromStyle

## Description
Updates the given plugin object from its style, if it has any.

```pascal
PROCEDURE UpdatePIOFromStyle(VAR pioHandle : HANDLE);
```

```python
def vs.UpdatePIOFromStyle():
    return pioHandle
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pioHandle|HANDLE|   |

## Examples
```pascal
createStyle := SetPluginStyle(borderH, titleBlockType);
UpdatePIOFromStyle(borderH);
```
```python
import vs

# Updates the given plugin object from its style, if it has any.
objHandle = vs.UpdatePIOFromStyle()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Utility](../Categories/Utility.md)
