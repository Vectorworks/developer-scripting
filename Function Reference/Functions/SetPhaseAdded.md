# SetPhaseAdded

## Description
Procedure SetPhaseAdded sets the passed in PhaseReference (long) as the added phase for the passed in handle.  If the passed in handle is not relocated, this function sets the created phase.  If the passed in handle is relocated, this function sets the relocated phase for the passed in handle.

```pascal
FUNCTION SetPhaseAdded(
				hObject  : HANDLE;
				phaseRef : LONGINT) : BOOLEAN;
```

```python
def vs.SetPhaseAdded(hObject, phaseRef):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The handle to set the added phase of.|
|phaseRef|LONGINT|The phase to set for the passed in object's added phase.|

## Returns
Returns a boolean to indicate a successful set of the added phase or a failure to set the added phase.

## See Also
VS Functions:
[GetPhaseAdded](GetPhaseAdded.md)| [GetPhaseRemoved](GetPhaseRemoved.md)| [SetPhaseRemoved](SetPhaseRemoved.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

