# CreateSlab

## Description
Creates a slab.

```pascal
FUNCTION CreateSlab(profile : HANDLE): HANDLE;
```

```python
def vs.CreateSlab(profile):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|profile|HANDLE|The profile from which to create the slab.|

## Examples
```pascal
resultH := CreateSlab(profile);
```
```python
import vs

# Creates a slab.
profile = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.CreateSlab(profile)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## See Also
VS Functions:
[ModifySlab](ModifySlab.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
