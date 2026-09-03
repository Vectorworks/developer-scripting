# Prot_GetLicenseID

## Description
Returns the license id.

```pascal
FUNCTION Prot_GetLicenseID : STRING;
```

```python
def vs.Prot_GetLicenseID():
    return STRING
```

## Examples
```pascal
resultStr := Prot_GetLicenseID;
```
```python
import vs

# Returns the license id.
text = vs.Prot_GetLicenseID()
vs.Message('Prot_GetLicenseID returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2023

## Category
* [Protection](../Categories/Protection.md)
