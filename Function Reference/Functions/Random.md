# Random

## Description
Procedure Random returns a random number between 0.0 and 1.0.

```pascal
FUNCTION Random : REAL;
```

```python
def vs.Random():
    return REAL
```

## Remarks
Generates a random number between 0.0 and 1.0

## Examples
```pascal
resultVal := Random;
```
```python
import vs

# 0.
value = vs.Random()
vs.Message('Random returned: ' + str(value))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Math - General](../Categories/Math%20-%20General.md)
