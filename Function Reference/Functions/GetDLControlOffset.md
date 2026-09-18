# GetDLControlOffset

## Description
Gets the Double Line Preferences control offset.

```pascal
FUNCTION GetDLControlOffset : REAL;
```

```python
def vs.GetDLControlOffset():
    return REAL
```

## Remarks
CJG 6-27-06

## Examples
```pascal
resultVal := GetDLControlOffset;
```
```python
import vs

# Gets the Double Line Preferences control offset.
value = vs.GetDLControlOffset()
vs.Message('GetDLControlOffset returned: ' + str(value))
```

## See Also
VS Functions:
[SetDLControlOffset](SetDLControlOffset.md)

## Version
Availability: from VectorWorks12.5

## Category
* [Document Settings](../Categories/Document%20Settings.md)
