# SetPhaseName

## Description
Procedure SetPhaseName takes in a PhaseReference (long) and a string and sets the passed in string as the new name for the passed in phase that has the ID of the passed in PhaseReference (long).

```pascal
FUNCTION SetPhaseName(
				phaseRef : LONGINT;
				nameStr  : STRING) : BOOLEAN;
```

```python
def vs.SetPhaseName(phaseRef, nameStr):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|phaseRef|LONGINT|The phase that the name is being set for.|
|nameStr|STRING|The name string to set for the passed in phase.|

## Returns
Returns a boolean to indicate a successful set of the phase name or a failure to set the phase name.

## See Also
VS Functions:
[GetPhaseName](GetPhaseName.md)| [GetPhaseDescription](GetPhaseDescription.md)| [SetPhaseDescription](SetPhaseDescription.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

