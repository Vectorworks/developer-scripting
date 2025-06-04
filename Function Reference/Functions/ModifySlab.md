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

## See Also
VS Functions:
[CreateSlab](CreateSlab.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
