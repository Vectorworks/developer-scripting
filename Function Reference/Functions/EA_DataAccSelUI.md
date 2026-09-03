# EA_DataAccSelUI

## Description
Selects item in popup and update system data.

```pascal
PROCEDURE EA_DataAccSelUI(
				acc      : INTEGER;
				dialogID : INTEGER;
				ctrlID   : INTEGER;
				uiIndex  : INTEGER);
```

```python
def vs.EA_DataAccSelUI(acc, dialogID, ctrlID, uiIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |
|dialogID|INTEGER|   |
|ctrlID|INTEGER|   |
|uiIndex|INTEGER|   |

## Examples
```pascal
EA_DataAccSelUI(1, 2, 3, 10);
```
```python
import vs

# Selects item in popup and update system data.
acc = 1
dialogID = 2
ctrlID = 3
uiIndex = 1

vs.EA_DataAccSelUI(acc, dialogID, ctrlID, uiIndex)
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
