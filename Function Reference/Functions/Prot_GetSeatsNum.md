# Prot_GetSeatsNum

## Description
Returns the number of Vectorworks seats licensed on the server.

```pascal
FUNCTION Prot_GetSeatsNum : INTEGER;
```

```python
def vs.Prot_GetSeatsNum():
    return INTEGER
```

## Examples
```pascal
resultN := Prot_GetSeatsNum;
```
```python
import vs

# Returns the number of Vectorworks seats licensed on the server.
count = vs.Prot_GetSeatsNum()
vs.Message('Prot_GetSeatsNum returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2015

## Category
* [Protection](../Categories/Protection.md)
