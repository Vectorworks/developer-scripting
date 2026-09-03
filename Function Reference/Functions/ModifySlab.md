# ModifySlab

## Description
Adds to or clips from a slab.

```pascal
FUNCTION ModifySlab(
				slab           : HANDLE;
				modifier       : HANDLE;
				isClipObject   : BOOLEAN;
				componentFlags : LONGINT): BOOLEAN;
```

```python
def vs.ModifySlab(slab, modifier, isClipObject, componentFlags):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|slab|HANDLE|The slab.|
|modifier|HANDLE|The adding or clipping object.|
|isClipObject|BOOLEAN|Whether the modifier is an add object or a clip object.|
|componentFlags|LONGINT|Bit flags that indicate which components will be affected by the modification.|

## Examples
```pascal
resultOK := ModifySlab(slab, modifier, TRUE, 1);
```
```python
import vs

# Adds to or clips from a slab.
slab = vs.FSActLayer()  # handle to the first selected object on the active layer
modifier = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
isClipObject = True
componentFlags = 1

ok = vs.ModifySlab(slab, modifier, isClipObject, componentFlags)
if ok:
    vs.Message('ModifySlab succeeded')
else:
    vs.Message('ModifySlab failed')
```

## See Also
VS Functions:
[CreateSlab](CreateSlab.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
