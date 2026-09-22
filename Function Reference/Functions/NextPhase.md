# NextPhase

## Description
Function NextPhase returns a PhaseReference (long) to the next phase in the document after the passed in phase.  If the passed in phase is not in the document, or is the last phase in the document, an invalid PhaseReference value is returned.

```pascal
FUNCTION NextPhase(phaseRef : LONGINT) : LONGINT;
```

```python
def vs.NextPhase(phaseRef):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|phaseRef|LONGINT|The phase to retrieve the next phase of.|

## See Also
VS Functions:
[PreviousPhase](PreviousPhase.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

