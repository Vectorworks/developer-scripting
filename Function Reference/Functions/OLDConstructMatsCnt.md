# OLDConstructMatsCnt

## Description
Returns the count of the construction materials available for truss analysis.

```pascal
FUNCTION OLDConstructMatsCnt : LONGINT;
```

```python
def vs.OLDConstructMatsCnt():
    return LONGINT
```

## Examples
```pascal
resultN := OLDConstructMatsCnt;
```
```python
import vs

# Returns the count of the construction materials available for truss analysis.
resultN = vs.OLDConstructMatsCnt()
vs.Message('OLDConstructMatsCnt returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
