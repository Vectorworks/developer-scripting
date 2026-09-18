# LObject

## Description
Function LObject returns a handle to the last object in the first layer of the active document.

```pascal
FUNCTION LObject : HANDLE;
```

```python
def vs.LObject():
    return HANDLE
```

## Examples
```pascal
resultH := LObject;
```
```python
import vs

# Function LObject returns a handle to the last object in the first layer of
# the active document.
objHandle = vs.LObject()
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
Relative calls:
* [NextObj](NextObj.md) | [PrevObj](PrevObj.md)
* [FObject](FObject.md) | [LObject](LObject.md)
* [FSActLayer](FSActLayer.md) | [LSActLayer](LSActLayer.md)
* [FSObject](FSObject.md)  | [LActLayer](LActLayer.md)
* [NextDObj](NextDObj.md) | [PrevDObj](PrevDObj.md)
* [NextSObj](NextSObj.md) | [PrevSObj](PrevSObj.md)

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
