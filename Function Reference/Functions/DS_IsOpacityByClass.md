# DS_IsOpacityByClass

## Description
Returns whether document shadow opacity is by class.

```pascal
FUNCTION DS_IsOpacityByClass : BOOLEAN;
```

```python
def vs.DS_IsOpacityByClass():
    return BOOLEAN
```

## Examples
```pascal
resultOK := DS_IsOpacityByClass;
```
```python
import vs

# Returns whether document shadow opacity is by class.
ok = vs.DS_IsOpacityByClass()
if ok:
    vs.Message('DS_IsOpacityByClass succeeded')
else:
    vs.Message('DS_IsOpacityByClass failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
