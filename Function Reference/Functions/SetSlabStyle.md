# SetSlabStyle

## Description
Sets the Slab Style of a slab.

```pascal
PROCEDURE SetSlabStyle(
				slab      : HANDLE;
				slabStyle : LONGINT);
```

```python
def vs.SetSlabStyle(slab, slabStyle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|slab|HANDLE|The slab.|
|slabStyle|LONGINT|The ref number of the Slab Style to apply to the slab. 0 for unstyled.|

## Examples
```pascal
SetSlabStyle(slab, 1);
```
```python
import vs

# Sets the Slab Style of a slab.
slab = vs.FSActLayer()  # handle to the first selected object on the active layer
slabStyle = 0

vs.SetSlabStyle(slab, slabStyle)
```

## See Also
VS Functions:
[GetSlabStyle](GetSlabStyle.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
