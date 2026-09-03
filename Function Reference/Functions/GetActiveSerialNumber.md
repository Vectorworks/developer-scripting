# GetActiveSerialNumber

## Description
Gets the currently active serial number.

```pascal
FUNCTION GetActiveSerialNumber : STRING;
```

```python
def vs.GetActiveSerialNumber():
    return STRING
```

## Examples
```pascal
resultStr := GetActiveSerialNumber;
```
```python
import vs

# Gets the currently active serial number.
text = vs.GetActiveSerialNumber()
vs.Message('GetActiveSerialNumber returned: ' + str(text))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Utility](../Categories/Utility.md)
