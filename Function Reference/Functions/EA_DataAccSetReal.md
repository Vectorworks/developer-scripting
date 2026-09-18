# EA_DataAccSetReal

## Description
Set real value to the object, associated to the accessory index.

```pascal
PROCEDURE EA_DataAccSetReal(
				acc        : INTEGER;
				valueIndex : INTEGER;
				value      : REAL);
```

```python
def vs.EA_DataAccSetReal(acc, valueIndex, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |
|valueIndex|INTEGER|   |
|value|REAL|   |

## Examples
```pascal
EA_DataAccSetReal(1, 2, 1.0);
```
```python
import vs

# Set real value to the object, associated to the accessory index.
acc = 1
valueIndex = 1
value = 1.0

vs.EA_DataAccSetReal(acc, valueIndex, value)
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
