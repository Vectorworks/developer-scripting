# EA_DataAccDelete

## Description
Destroys accessory by index. The function closes the 'session' to energy analysis plugin for particular handle. The handle is a handle to record format or to object.

```pascal
PROCEDURE EA_DataAccDelete(acc : INTEGER);
```

```python
def vs.EA_DataAccDelete(acc):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |

## Examples
```pascal
EA_DataAccDelete(1);
```
```python
import vs

# Destroys accessory by index.
acc = 1

vs.EA_DataAccDelete(acc)
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
