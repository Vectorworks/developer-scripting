# Prot_GetLicenseType

## Description
Returns the license type Vectorworks is using.

```pascal
FUNCTION Prot_GetLicenseType : LONGINT;
```

```python
def vs.Prot_GetLicenseType():
    return LONGINT
```

## Examples
```pascal
resultN := Prot_GetLicenseType;
```
```python
import vs

# Returns the license type Vectorworks is using.
resultN = vs.Prot_GetLicenseType()
vs.Message('Prot_GetLicenseType returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2023

## Category
* [Protection](../Categories/Protection.md)
