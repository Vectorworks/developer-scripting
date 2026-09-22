# SetActivePhase

## Description
Procedure SetActivePhase sets the passed in phase as the active phase in the document.  If an invalid phase is passed in, the active phase is not changed.

```pascal
FUNCTION SetActivePhase(phaseRef : LONGINT) : BOOLEAN;
```

```python
def vs.SetActivePhase(phaseRef):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|phaseRef|LONGINT|The phase to set as the active phase of the drawing.|

## Returns
Returns a boolean to indicate a successful set of the active phase or a failure to set the active phase.

## See Also
VS Functions:
[GetActivePhase](GetActivePhase.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Phasing](Categories/Phasing.md)

