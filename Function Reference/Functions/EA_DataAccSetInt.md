# EA_DataAccSetInt

## Description
Set integer value to the object, associated to the accessory index.

```pascal
PROCEDURE EA_DataAccSetInt(
				acc        : INTEGER;
				valueIndex : INTEGER;
				value      : INTEGER);
```

```python
def vs.EA_DataAccSetInt(acc, valueIndex, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |
|valueIndex|INTEGER|   |
|value|INTEGER|   |

## Examples
```pascal
EA_DataAccSetInt(1, 2, 3);
```
```python
import vs

# Set integer value to the object, associated to the accessory index.
acc = 1
valueIndex = 1
value = 2

vs.EA_DataAccSetInt(acc, valueIndex, value)
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
