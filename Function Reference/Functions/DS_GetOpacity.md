# DS_GetOpacity

## Description
Returns document shadow opacity.

```pascal
FUNCTION DS_GetOpacity : LONGINT;
```

```python
def vs.DS_GetOpacity():
    return LONGINT
```

## Examples
```pascal
resultN := DS_GetOpacity;
```
```python
import vs

# Returns document shadow opacity.
resultN = vs.DS_GetOpacity()
vs.Message('DS_GetOpacity returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
