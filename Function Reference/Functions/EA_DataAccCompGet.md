# EA_DataAccCompGet

## Description
Gets object component data.

```pascal
PROCEDURE EA_DataAccCompGet(
				acc                : INTEGER;
				VAR componentIndex : INTEGER;
				VAR outInclude     : BOOLEAN;
				VAR outLambda      : REAL;
				VAR outThickness   : REAL);
```

```python
def vs.EA_DataAccCompGet(acc):
    return (componentIndex, outInclude, outLambda, outThickness)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|acc|INTEGER|   |
|componentIndex|INTEGER|   |
|outInclude|BOOLEAN|   |
|outLambda|REAL|   |
|outThickness|REAL|   |

## Remarks
(*\_c\_*, 2022.04.14):
Python only: EA_DataAccCompGet can't be used for VW before 2022 SP4, the index returned is gibberish. 

An extensive example about the Energos access can be found under [[VS:EA DataAccCreate]]

## Examples
```pascal
EA_DataAccCompGet(1, 2, TRUE, 1.0, 2.0);
```
```python
import vs

# Gets object component data.
acc = 1

componentIndex, outInclude, outLambda, outThickness = vs.EA_DataAccCompGet(acc)
vs.Message('EA_DataAccCompGet returned: ' + str((componentIndex, outInclude, outLambda, outThickness)))
```

## Version
Availability: from Vectorworks 2016

## Category
* [EnergyAnalysis Interface Library](../Categories/EnergyAnalysis%20Interface%20Library.md)
