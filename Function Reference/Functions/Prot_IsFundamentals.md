# Prot_IsFundamentals

## Description
Returns true if we only have a fundamentals license enabled.

```pascal
FUNCTION Prot_IsFundamentals : BOOLEAN;
```

```python
def vs.Prot_IsFundamentals():
    return BOOLEAN
```

## Examples
```pascal
resultOK := Prot_IsFundamentals;
```
```python
import vs

# Returns true if we only have a fundamentals license enabled.
ok = vs.Prot_IsFundamentals()
if ok:
    vs.Message('Prot_IsFundamentals succeeded')
else:
    vs.Message('Prot_IsFundamentals failed')
```

## Version
Availability: from Vectorworks 2023

## Category
* [Protection](../Categories/Protection.md)
