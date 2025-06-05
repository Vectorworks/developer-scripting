# PenPat

## Description
<b>Use [[VS:PenPatN|PenPatN]] instead. </b>
Procedure PenPat sets the active pen pattern (line style) for the document.

If patNumber is in the range 0 to 71 the linestyle will be set to the corresponding fill pattern. A value in the range -1 to -8, will set the linestyle to one of the defined VectorWorks linestyles.

Fill patterns and their associated constants can be found in the [VectorScript Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#fill-patterns).

```pascal
PROCEDURE PenPat(patNumber : INTEGER);
```

```python
def vs.PenPat(patNumber):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|patNumber|INTEGER|Pattern/linestyle ID value.|

## Examples
#### VectorScript ####
```pascal
PenPat(25);
{ uses fill pattern 25 as the active pen pattern }

PenPat(-3);
{ sets a linestyle as the active pen pattern }
```
#### Python ####
```python

```

## See Also
[PenPatN|PenPatN](PenPatN|PenPatN.md), [FPenPatN|FPenPatN](FPenPatN|FPenPatN.md) from Vectorworks 2013

## Version
Availability: from All Versions, deprecated from Vectorworks 2013

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
