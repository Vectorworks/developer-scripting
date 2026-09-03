# Prot_GetAppMode

## Description
Returns the application mode Vectorworks is using.

```pascal
FUNCTION Prot_GetAppMode : LONGINT;
```

```python
def vs.Prot_GetAppMode():
    return LONGINT
```

## Examples
```pascal
resultN := Prot_GetAppMode;
```
```python
import vs

# Returns the application mode Vectorworks is using.
resultN = vs.Prot_GetAppMode()
vs.Message('Prot_GetAppMode returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2023

## Category
* [Protection](../Categories/Protection.md)
