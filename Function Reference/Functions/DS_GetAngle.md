# DS_GetAngle

## Description
Returns document shadow angle.

```pascal
FUNCTION DS_GetAngle : REAL;
```

```python
def vs.DS_GetAngle():
    return REAL
```

## Examples
```pascal
resultVal := DS_GetAngle;
```
```python
import vs

# Returns document shadow angle.
angle = vs.DS_GetAngle()
vs.Message('DS_GetAngle returned: ' + str(angle))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
