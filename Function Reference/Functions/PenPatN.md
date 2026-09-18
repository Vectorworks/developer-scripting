# PenPatN

## Description
Procedure PenPatN sets the active pen pattern (line style) for the document.

If patNumber is in the range 0 to 71 the linestyle will be set to the corresponding fill pattern. A negative value, will set the linestyle to the line type resource whose index is the negative of the value.

```pascal
PROCEDURE PenPatN(patNumber : LONGINT);
```

```python
def vs.PenPatN(patNumber):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|patNumber|LONGINT|Pattern/linestyle ID value.|

## Remarks
*\_c\_* (2016.02.29): VS:FPenPatN requires a name list index, while the older routine VS:PenPat requires the dash style index. Please mind that a document doesn't necessarily have dash styles loaded.

```pascal
PenPatN(-Name2Index('ISO-02 Dashed')); { makes 'ISO-02 Dashed' as the active pen pattern }
```

## Examples
```pascal
PenPatN(25);
{ uses fill pattern 25 as the active pen pattern }

indx := Name2Index('ISO-02 Dashed');
PenPatN(-indx);
{ makes 'ISO-02 Dashed' as the active pen pattern }
```

```pascal
	PenPatN(CurrentPenPat);
END

BEGIN
	GetPenFore (gWallHand,r,g,b);
	PenFore (r,g,b);
	Pensize (GetLW (gWallHand));
	PenPatN (GetLSN (gWallHand));
	GetFillBack (gWallHand,r,g,b);
	FillBack (r,g,b);
END;

savePenPat := FPenPatN;
savePenSize := FPenSize;
FPenFore(saveR, saveG, saveB);
PenPatN(gLeaderType);
PenSize(gLeaderThickness);
GetPenFore(ActiveParmHand, r, g, b);
PenFore(r, g, b);
MoveTo(bubbleIntPt.x, bubbleIntPt.y);
```
```python
if not vs.IsLSByClass( objHand ):
	penPat	= vs.GetLSN( objHand )
	vs.PenPatN( penPat )
```

## See Also
VS Functions:
[FPenPatN](FPenPatN.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
