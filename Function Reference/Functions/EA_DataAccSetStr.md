# EA_DataAccSetStr

## Description
Set string value to the object, associated to the accessory index.

```pascal
PROCEDURE EA_DataAccSetStr(
				acc        : INTEGER;
				valueIndex : INTEGER;
				value      : STRING);
```

```python
def vs.EA_DataAccSetStr(acc, valueIndex, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |
|valueIndex|INTEGER|   |
|value|STRING|   |

## Examples
```pascal
EA_DataAccSetStr(1, 2, 'Example');
```
```python
import vs

# Set string value to the object, associated to the accessory index.
acc = 1
valueIndex = 1
value = 'Example'

vs.EA_DataAccSetStr(acc, valueIndex, value)
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
