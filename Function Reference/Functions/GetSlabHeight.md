# GetSlabHeight

## Description
Gets the height of a slab.

```pascal
FUNCTION GetSlabHeight(slab : HANDLE): REAL;
```

```python
def vs.GetSlabHeight(slab):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|slab|HANDLE|The slab.|

## Examples
```pascal
resultVal := GetSlabHeight(slab);
```
```python
import vs

# Gets the height of a slab.
slab = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.GetSlabHeight(slab)
vs.Message('GetSlabHeight returned: ' + str(value))
```

## See Also
VS Functions:
[SetSlabHeight](SetSlabHeight.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
