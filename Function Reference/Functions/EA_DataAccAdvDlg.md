# EA_DataAccAdvDlg

## Description
Shows an advanced settings dialog.

```pascal
FUNCTION EA_DataAccAdvDlg(acc : INTEGER): BOOLEAN;
```

```python
def vs.EA_DataAccAdvDlg(acc):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |

## Examples
```pascal
resultOK := EA_DataAccAdvDlg(1);
```
```python
import vs

# Shows an advanced settings dialog.
acc = 1

ok = vs.EA_DataAccAdvDlg(acc)
if ok:
    vs.Message('EA_DataAccAdvDlg succeeded')
else:
    vs.Message('EA_DataAccAdvDlg failed')
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
