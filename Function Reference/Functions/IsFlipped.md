# IsFlipped

## Description
Returns the number of objects meeting the criteria that are flipped.

```pascal
FUNCTION IsFlipped(c : CRITERIA): REAL;
```

```python
def vs.IsFlipped(c):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Remarks
This function returns true? if the object matching the given criteria (such as a symbol is flipped.  Only certain types of objects can be flipped.

The change to criteria for this seems weird; does it accumulate the flipped states of the objects matching the criteria and return the sum?

## Examples
==== VectorScript ====
```pascal
PROCEDURE CountFlippedDoorSymbols;
BEGIN
Message(IsFlipped(S='*Door*'));
END;
RUN(CountFlippedDoorSymbols);
```
==== Python ====
```python

```

## See Also
VS Functions:
[IsObjectFlipped](IsObjectFlipped.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Criteria](../Categories/Criteria.md)
