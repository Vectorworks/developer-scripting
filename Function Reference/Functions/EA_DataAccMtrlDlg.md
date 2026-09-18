# EA_DataAccMtrlDlg

## Description
Shows the lambda material dialog and set the selected lambda value to outLambda.

```pascal
FUNCTION EA_DataAccMtrlDlg(
				acc           : INTEGER;
				VAR outLambda : REAL): BOOLEAN;
```

```python
def vs.EA_DataAccMtrlDlg(acc):
    return (BOOLEAN, outLambda)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |
|outLambda|REAL|   |

## Examples
```pascal
resultOK := EA_DataAccMtrlDlg(1, 1.0);
```
```python
import vs

# Shows the lambda material dialog and set the selected lambda value to
# outLambda.
acc = 1

ok, outLambda = vs.EA_DataAccMtrlDlg(acc)
vs.Message('EA_DataAccMtrlDlg returned: ' + str((ok, outLambda)))
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
