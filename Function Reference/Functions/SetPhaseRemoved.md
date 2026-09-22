# SetPhaseRemoved

## Description
Procedure SetPhaseRemoved sets the passed in PhaseReference (long) as the removed phase for the passed in handle.

```pascal
FUNCTION SetPhaseRemoved(
				hObject  : HANDLE;
				phaseRef : LONGINT) : BOOLEAN;
```

```python
def vs.SetPhaseRemoved(hObject, phaseRef):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The handle to set the removed phase of.|
|phaseRef|LONGINT|The phase to set for the passed in object's removed phase.|

## Returns
Returns a boolean to indicate a successful set of the removed phase or a failure to set the removed phase.

## See Also
VS Functions:
[GetPhaseRemoved](GetPhaseRemoved.md)| [GetPhaseAdded](GetPhaseAdded.md)| [SetPhaseAdded](SetPhaseAdded.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

