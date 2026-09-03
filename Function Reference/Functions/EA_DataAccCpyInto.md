# EA_DataAccCpyInto

## Description
Copies data from accessory to object.

```pascal
PROCEDURE EA_DataAccCpyInto(
				acc : INTEGER;
				h   : HANDLE);
```

```python
def vs.EA_DataAccCpyInto(acc, h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |
|h|HANDLE|   |

## Examples
```pascal
EA_DataAccCpyInto(1, h);
```
```python
import vs

# Copies data from accessory to object.
acc = 1
h = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.EA_DataAccCpyInto(acc, h)
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
