# NameNum

## Description
Function NameNum returns the number of different object names in the active VectorWorks document.

```pascal
FUNCTION NameNum : LONGINT;
```

```python
def vs.NameNum():
    return LONGINT
```

## Examples
```pascal
resultN := NameNum;
```
```python
import vs

# Function NameNum returns the number of different object names in the active
# VectorWorks document.
count = vs.NameNum()
vs.Message('NameNum returned: ' + str(count))
```

## Version
Availability: from All Versions

## Category
* [Object Names](../Categories/Object%20Names.md)
