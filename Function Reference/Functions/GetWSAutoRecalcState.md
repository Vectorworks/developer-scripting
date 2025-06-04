# GetWSAutoRecalcState

## Description
Gets the AutoRecalc state for the specified worksheet.<BR>
<BR>
When the AutoRecalc flag is on for a worksheet, it automatically recalculates every time a cell is edited.<BR>
<BR>
In order to improve speed when editing mutiple cells one after the other or in a loop, it is highly recommended to turn this flag off prior to the edits and restore it, then recalculate the worksheet when all the edits are completed.

```pascal
FUNCTION GetWSAutoRecalcState(worksheet : HANDLE): BOOLEAN;
```

```python
def vs.GetWSAutoRecalcState(worksheet):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|

## Examples
==== VectorScript ====
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
==== Python ====
```python
#{Save the current AutoRecalc state}
state = vs.GetWSAutoRecalcState(h)

#{Turn off worksheet Auto Recalculation}
vs.SetWSAutoRecalcState(h,False)

#{Execute worksheet edit operations ....}

#{Restore AutoRecalc state}
vs.SetWSAutoRecalcState(h, state)

#{Recalculate the worksheet}
vs.RecalculateWS(h)
```

## See Also
VS Functions:
[SetWSAutoRecalcState](SetWSAutoRecalcState.md) 
| [RecalculateWS](RecalculateWS.md)

## Version
Availability: from Vectorworks 14.0

## Category
* [Worksheets](../Categories/Worksheets.md)
