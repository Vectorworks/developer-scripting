# FPenPatN

## Description
Function FPenPatN returns the active pen pattern setting.

```pascal
FUNCTION FPenPatN : LONGINT;
```

```python
def vs.FPenPatN():
    return LONGINT
```

## Remarks
*\_c\_* (2016.02.29): [FPenPatN](FPenPatN.md) returns the name list index of the active dash style, while the older routine [FPenPat](FPenPat.md) will return the dash style index. They are not the same.

<code lang='vs'>
{ compare the two different indexes: }
indx := FPenPat; { returns the dash style list index corresponding to the active dash style }
indx := FPenPatN; { returns the name list index corresponding to the active dash style }
```

## See Also
VS Functions:
[PenPatN](PenPatN.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
