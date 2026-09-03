# CreateSlabStyle

## Description
Creates a new Slab Style of the given name. If the name is already in use, the next available name will be used.

```pascal
FUNCTION CreateSlabStyle(slabStyleName : STRING): HANDLE;
```

```python
def vs.CreateSlabStyle(slabStyleName):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|slabStyleName|STRING|The name of the new Slab Style.  If the name is already in use, the next available name will be used.|

## Examples
```pascal
resultH := CreateSlabStyle('Example');
```
```python
import vs

# Creates a new Slab Style of the given name.
slabStyleName = 'Example'

objHandle = vs.CreateSlabStyle(slabStyleName)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
