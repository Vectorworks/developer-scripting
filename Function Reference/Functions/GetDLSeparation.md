# GetDLSeparation

## Description
Gets the Double Line Preferences separation.

```pascal
FUNCTION GetDLSeparation : REAL;
```

```python
def vs.GetDLSeparation():
    return REAL
```

## Remarks
CJG 6-27-06

## Examples
```pascal
resultVal := GetDLSeparation;
```
```python
import vs

# Gets the Double Line Preferences separation.
value = vs.GetDLSeparation()
vs.Message('GetDLSeparation returned: ' + str(value))
```

## See Also
VS Functions:
[SetDLSeparation](SetDLSeparation.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
