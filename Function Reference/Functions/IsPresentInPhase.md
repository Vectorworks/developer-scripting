# IsPresentInPhase

## Description
Function IsPresentInPhase takes in a handle and a PhaseReference (long) and returns a boolean indicating whether the passed in handle exists in the passed in phase.

```pascal
FUNCTION IsPresentInPhase(
				hObject  : HANDLE;
				phaseRef : LONGINT) : BOOLEAN;
```

```python
def vs.IsPresentInPhase(hObject, phaseRef):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The object to determine the existence for.|
|phaseRef|LONGINT|The phase to use for determining whether the passed in object exists or not.|

## See Also
VS Functions:
[GetPhaseStatus](GetPhaseStatus.md)| [GetStatusInPhase](GetStatusInPhase.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

