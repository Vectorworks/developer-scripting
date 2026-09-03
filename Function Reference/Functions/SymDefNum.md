# SymDefNum

## Description
Function SymDefNum returns the number of symbol definitions within the active document.

```pascal
FUNCTION SymDefNum : LONGINT;
```

```python
def vs.SymDefNum():
    return LONGINT
```

## Examples
```pascal
resultN := SymDefNum;
```
```python
import vs

# Function SymDefNum returns the number of symbol definitions within the
# active document.
count = vs.SymDefNum()
vs.Message('SymDefNum returned: ' + str(count))
```

## Version
Availability: from All Versions

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
