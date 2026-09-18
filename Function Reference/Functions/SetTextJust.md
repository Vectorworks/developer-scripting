# SetTextJust

## Description
Procedure SetTextJust sets the text justification of the referenced text object. 

![Text Locus](files/Textlocus.gif)

**Table - Text Justification**

| Justification | Constant |
|---------------|----------|
| Left          | 1        |
| Center        | 2        |
| Right         | 3        |
| Justify       | 4        |

```pascal
PROCEDURE SetTextJust(
				TextHd   : HANDLE;
				JustFlag : INTEGER);
```

```python
def vs.SetTextJust(TextHd, JustFlag):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|TextHd|HANDLE|Handle to text object.|
|JustFlag|INTEGER|Justification setting for text.|

## Remarks
([[User:Orso.b.schmid|Orso]], 2012 Mai. 26): The constant 4 "Justify" is introduced by VW 2011. This routine needs a screen redraw after running. The text object will shift after changing the alignment, use [SetTextJustN](SetTextJustN.md) if the shift is not wished.

## Examples
```pascal
SetFPat(LNewObj,0);
angle:=angle*PI/(2*180);
Moveto(Sin(angle)*rad,cos(angle)*rad);
CreateText(anno);
SetTextJust(LNewObj,2);
SetTextVerticalAlign(LNewObj,3);
setfpat(lnewobj,GetFPat(parmHand));
GetFillBack(parmHand,red,grn,bl);
SetFillBack(LNewObj,red,grn,bl);

BEGIN
	TextOrigin(pControlPoint01X, pControlPoint01Y);
	CreateText(pColumn_ID);
	SetTextVerticalAlign(LNewObj, 3);
	SetTextJust(LNewObj, 2);

	SetRField(objectHand, kSeatingObjectName, 'Symbol', SeatSymName);
	SetRField(objectHand, kSeatingObjectName, 'UpdateWS', 'FALSE');
	SetMinSpacing(objectHand);
	SetVersion(objectHand, kSeatingObjectName);
	SetTextJust(ObjectHand,2);
	SetTextVerticalAlign(ObjectHand,3);
	ResetObject(ObjectHand);
	CreateSeatLayoutObj := ObjectHand;
END
```
```python
textHand = vs.LNewObj()
vs.SetTextJust( textHand, 2 )
vs.SetTextVerticalAlign( textHand, 5)

vs.BeginGroup()
vs.CreateText( message1 )
vs.SetTextVerticalAlign( vs.LNewObj(), 3 )
vs.SetTextJust( vs.LNewObj(), 2 )
vs.SetPenFore( vs.LNewObj(), 65535, 0, 0 )
vs.SetFPat( vs.LNewObj(), 0 )
b1, b2 = vs.GetBBox( vs.LNewObj() )
vs.Rect( kBf * b1[0], kBf * b1[1], kBf * b2[0], kBf * b2[1] )
```

## See Also
VS Functions:
* [GetTextJust](GetTextJust.md) | [SetTextJustN](SetTextJustN.md) 
* [GetTextVerticalAlign](GetTextVerticalAlign.md) | [SetTextVerticalAlign](SetTextVerticalAlign.md)

## Version
Availability: from MiniCAD 6.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
