# GetPhaseAdded

## Description
Function GetPhaseAdded takes in a handle and returns the phase when the passed in handle was added to the document.  If the passed in handle is not relocated, this function returns the created phase.  If the passed in handle is relocated, this function returns the relocated phase for the passed in handle.

```pascal
FUNCTION GetPhaseAdded(hObject : HANDLE) : LONGINT;
```

```python
def vs.GetPhaseAdded(hObject):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The handle to retrieve the created (or relocated) phase for.|

## See Also
VS Functions:
[SetPhaseAdded](SetPhaseAdded.md)| [GetPhaseRemoved](GetPhaseRemoved.md)| [SetPhaseRemoved](SetPhaseRemoved.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

