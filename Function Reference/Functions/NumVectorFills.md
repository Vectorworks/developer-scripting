# NumVectorFills

## Description
Function NumVectorFills returns the number of vector fills in the active document.

```pascal
FUNCTION NumVectorFills : LONGINT;
```

```python
def vs.NumVectorFills():
    return LONGINT
```

## Remarks
Returns with the number of vector fills in the active document.

## Examples
```pascal
resultN := NumVectorFills;
```
```python
import vs

# Function NumVectorFills returns the number of vector fills in the active
# document.
count = vs.NumVectorFills()
vs.Message('NumVectorFills returned: ' + str(count))
```

## Version
Availability: from MiniCAD7.0.1

## Category
* [Hatches @ Vector Fills](../Categories/Hatches%20-%20Vector%20Fills.md)
