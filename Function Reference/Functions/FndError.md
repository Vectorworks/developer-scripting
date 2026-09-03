# FndError

## Description
Function FndError returns whether an error has occurred within a VectorScript subroutine. Provided as a debugging tool, FndError receives notification after execution of every line of code whether an error has occurred.

```pascal
FUNCTION FndError : BOOLEAN;
```

```python
def vs.FndError():
    return BOOLEAN
```

## Remarks
This example isn't very helpful. JDW.
[sd 8/14/98]

## Examples
```pascal
resultOK := FndError;
```
```python
import vs

# Function FndError returns whether an error has occurred within a
# VectorScript subroutine.
ok = vs.FndError()
if ok:
    vs.Message('FndError succeeded')
else:
    vs.Message('FndError failed')
```

## Version
Availability: from All Versions

## Category
* [Utility](../Categories/Utility.md)
