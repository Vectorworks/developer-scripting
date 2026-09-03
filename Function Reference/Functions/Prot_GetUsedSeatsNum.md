# Prot_GetUsedSeatsNum

## Description
Returns the number of running Vectorworks on the network.

```pascal
FUNCTION Prot_GetUsedSeatsNum : INTEGER;
```

```python
def vs.Prot_GetUsedSeatsNum():
    return INTEGER
```

## Examples
```pascal
resultN := Prot_GetUsedSeatsNum;
```
```python
import vs

# Returns the number of running Vectorworks on the network.
count = vs.Prot_GetUsedSeatsNum()
vs.Message('Prot_GetUsedSeatsNum returned: ' + str(count))
```

## Version
Availability: from Vectorworks 2015

## Category
* [Protection](../Categories/Protection.md)
