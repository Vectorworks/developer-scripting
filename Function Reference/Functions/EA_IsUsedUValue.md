# EA_IsUsedUValue

## Description
Returns TRUE if U-Value is used. If R-value is used returns FALSE.

```pascal
FUNCTION EA_IsUsedUValue : BOOLEAN;
```

```python
def vs.EA_IsUsedUValue():
    return BOOLEAN
```

## Examples
```pascal
resultOK := EA_IsUsedUValue;
```
```python
import vs

# Returns TRUE if U-Value is used.
ok = vs.EA_IsUsedUValue()
if ok:
    vs.Message('EA_IsUsedUValue succeeded')
else:
    vs.Message('EA_IsUsedUValue failed')
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
