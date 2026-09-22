# SetPhaseDescription

## Description
Procedure SetPhaseDescription takes in a PhaseReference (long) and a string and sets the passed in string as the new description for the passed in phase that has the ID of the passed in PhaseReference (long).

```pascal
FUNCTION SetPhaseDescription(
				phaseRef       : LONGINT;
				descriptionStr : STRING) : BOOLEAN;
```

```python
def vs.SetPhaseDescription(phaseRef, descriptionStr):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|phaseRef|LONGINT|The phase to set the description for.|
|descriptionStr|STRING|The description string to set for the passed in phase.|

## Returns
Returns a boolean to indicate a successful set of the phase description or a failure to set the phase description.

## See Also
VS Functions:
[GetPhaseDescription](GetPhaseDescription.md)| [GetPhaseName](GetPhaseName.md)| [SetPhaseName](SetPhaseName.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

