# Space_FullyReset

## Description
Allow a full rest of the Space obj, including Boundary

```pascal
PROCEDURE Space_FullyReset(space : HANDLE);
```

```python

def vs.Space_FullyReset(space):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE||

## Examples
```pascal
Space_FullyReset(space);
```
```python
import vs

# Allow a full rest of the Space obj, including Boundary.
space = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.Space_FullyReset(space)
```

## Version
Availability: from Vectorworks 2024

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
