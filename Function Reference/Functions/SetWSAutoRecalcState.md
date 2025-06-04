# SetWSAutoRecalcState

## Description
Sets the AutoRecalc flag for the specified worksheet.

```pascal
PROCEDURE SetWSAutoRecalcState(
				worksheet : HANDLE;
				state     : BOOLEAN);
```

```python
def vs.SetWSAutoRecalcState(worksheet, state):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|state|BOOLEAN|Worksheet AutoRecalc flag.|

## Examples
#### VectorScript ####
```pascal
{Save the current AutoRecalc state}
state := GetWSAutoRecalcState(h);

{Turn off worksheet Auto Recalculation}
SetWSAutoRecalcState(h,false);

{Execute worksheet edit operations ....}

{Restore AutoRecalc state}
SetWSAutoRecalcState(h, state);

{Recalculate the worksheet}
RecalculateWS(h);
```
#### Python ####
```python

```

## See Also
VS Functions:
[GetWSAutoRecalcState](GetWSAutoRecalcState.md) 
| [RecalculateWS](RecalculateWS.md)

## Version
Availability: from Vectorworks14.0

## Category
* [Worksheets](../Categories/Worksheets.md)
