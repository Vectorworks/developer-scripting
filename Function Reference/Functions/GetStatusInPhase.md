# GetStatusInPhase

## Description
Function GetStatusInPhase takes in a handle and a PhaseReference (long) and returns a string indicating the handle's phasing status in the passed in phase.

```pascal
FUNCTION GetStatusInPhase(
				hObject  : HANDLE;
				phaseRef : LONGINT) : STRING;
```

```python
def vs.GetStatusInPhase(hObject, phaseRef):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The object to get the status of.|
|phaseRef|LONGINT|The phase to use for retrieving the objects status.|

## See Also
VS Functions:
[GetPhaseStatus](GetPhaseStatus.md)| [IsPresentInPhase](IsPresentInPhase.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

