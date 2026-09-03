# SetSlabHeight

## Description
Sets the height of a slab.

```pascal
PROCEDURE SetSlabHeight(
				slab   : HANDLE;
				height : REAL);
```

```python
def vs.SetSlabHeight(slab, height):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|slab|HANDLE|The slab.|
|height|REAL|The height of the slab.|

## Examples
```pascal
SetSlabHeight(slab, 1.0);
```
```python
import vs

# Sets the height of a slab.
slab = vs.FSActLayer()  # handle to the first selected object on the active layer
height = 2.0

vs.SetSlabHeight(slab, height)
```

## See Also
VS Functions:
[GetSlabHeight](GetSlabHeight.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
