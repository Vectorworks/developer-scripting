# GetPhaseRemoved

## Description
Function GetPhaseRemoved takes in a handle and returns the phase when the passed in handle was removed from the document.  If the passed in handle is not removed from the document, this function returns a "None" value.

```pascal
FUNCTION GetPhaseRemoved(hObject : HANDLE) : LONGINT;
```

```python
def vs.GetPhaseRemoved(hObject):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|The handle to retrieve the removed phase for.|

## See Also
VS Functions:
[SetPhaseRemoved](SetPhaseRemoved.md)| [GetPhaseAdded](GetPhaseAdded.md)| [SetPhaseAdded](SetPhaseAdded.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

