# ConvertToUnstyledSlab

## Description
Sets a slab to be unstyled.

```pascal
PROCEDURE ConvertToUnstyledSlab(slab : HANDLE);
```

```python
def vs.ConvertToUnstyledSlab(slab):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|slab|HANDLE|The slab.|

## Examples
```pascal
ConvertToUnstyledSlab(slab);
```
```python
import vs

# Sets a slab to be unstyled.
slab = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.ConvertToUnstyledSlab(slab)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
