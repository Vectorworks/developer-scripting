# PreviousPhase

## Description
Function PreviousPhase returns a PhaseReference (long) to the previous phase in the document before the passed in phase. If the passed in phase is the "<None>" phase, the last phase in the document is returned.  If the passed in phase is not in the document, or is the first phase in the document, an invalid PhaseReference value is returned.

```pascal
FUNCTION PreviousPhase(phaseRef : LONGINT) : LONGINT;
```

```python
def vs.PreviousPhase(phaseRef):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|phaseRef|LONGINT|The phase to retrieve the previous phase of.|

## See Also
VS Functions:
[NextPhase](NextPhase.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

