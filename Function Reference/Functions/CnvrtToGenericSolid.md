# CnvrtToGenericSolid

## Description
Converts Solid objects to generic solids. Removes solid history saving memory.

```pascal
FUNCTION CnvrtToGenericSolid(solid : HANDLE): HANDLE;
```

```python
def vs.CnvrtToGenericSolid(solid):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|solid|HANDLE|object to convert|

## Examples
```pascal
resultH := CnvrtToGenericSolid(solid);
```
```python
import vs

# Converts Solid objects to generic solids.
solid = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.CnvrtToGenericSolid(solid)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Solids](../Categories/Objects%20-%20Solids.md)
