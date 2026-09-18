# IsRW

## Description
Indicates whether RenderWorks is available.

```pascal
FUNCTION IsRW : BOOLEAN;
```

```python
def vs.IsRW():
    return BOOLEAN
```

## Examples
```pascal
resultOK := IsRW;
```
```python
import vs

# Indicates whether RenderWorks is available.
ok = vs.IsRW()
if ok:
    vs.Message('IsRW succeeded')
else:
    vs.Message('IsRW failed')
```

## Version
Availability: from VectorWorks10.0

## Category
* [Textures](../Categories/Textures.md)
