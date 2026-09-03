# DS_IsUnderCanopy

## Description
Returns whether document shadow is under Canopy.

```pascal
FUNCTION DS_IsUnderCanopy : BOOLEAN;
```

```python
def vs.DS_IsUnderCanopy():
    return BOOLEAN
```

## Examples
```pascal
resultOK := DS_IsUnderCanopy;
```
```python
import vs

# Returns whether document shadow is under Canopy.
ok = vs.DS_IsUnderCanopy()
if ok:
    vs.Message('DS_IsUnderCanopy succeeded')
else:
    vs.Message('DS_IsUnderCanopy failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
