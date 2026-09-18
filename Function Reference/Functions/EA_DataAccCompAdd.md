# EA_DataAccCompAdd

## Description
Adds object component.

```pascal
PROCEDURE EA_DataAccCompAdd(
				acc       : INTEGER;
				include   : BOOLEAN;
				lambda    : REAL;
				thickness : REAL);
```

```python
def vs.EA_DataAccCompAdd(acc, include, lambda, thickness):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |
|include|BOOLEAN|   |
|lambda|REAL|   |
|thickness|REAL|   |

## Examples
```pascal
EA_DataAccCompAdd(1, TRUE, 1.0, 2.0);
```
```python
import vs

# Adds object component.
acc = 1
include = True
lambda = 1.0
thickness = 0.1

vs.EA_DataAccCompAdd(acc, include, lambda, thickness)
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
