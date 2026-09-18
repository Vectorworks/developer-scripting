# SetTextVerticalAlign

## Description
Procedure SetTextVerticalAlign sets the vertical alignment of the referenced text object. 

![Text Locus](files/Textlocus.gif)

**Table - Text Vertical Justification**

| Justification        | Constant |
|----------------------|----------|
| Top of text box      | 1        |
| Top baseline         | 2        |
| Text centerline      | 3        |
| Bottom baseline      | 4        |
| Bottom of text box   | 5        |

```pascal
PROCEDURE SetTextVerticalAlign(
				TextHd            : HANDLE;
				verticalAlignment : INTEGER);
```

```python
def vs.SetTextVerticalAlign(TextHd, verticalAlignment):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|TextHd|HANDLE|Handle to text object.|
|verticalAlignment|INTEGER|Vertical alignment setting for text.|

## Remarks
This routine needs a screen redraw after running. The text object will shift after changing the alignment, use [SetTextVertAlignN](SetTextVertAlignN.md) if the shift is not wished.

## Examples
```pascal
angle:=angle*PI/(2*180);
Moveto(Sin(angle)*rad,cos(angle)*rad);
CreateText(anno);
SetTextJust(LNewObj,2);
SetTextVerticalAlign(LNewObj,3);
setfpat(lnewobj,GetFPat(parmHand));
GetFillBack(parmHand,red,grn,bl);
SetFillBack(LNewObj,red,grn,bl);
popattrs;

BEGIN
	TextOrigin(pControlPoint01X, pControlPoint01Y);
	CreateText(pColumn_ID);
	SetTextVerticalAlign(LNewObj, 3);
	SetTextJust(LNewObj, 2);

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

vs.MoveTo( 0, 0 )
vs.BeginGroup()
vs.CreateText( message1 )
vs.SetTextVerticalAlign( vs.LNewObj(), 3 )
vs.SetTextJust( vs.LNewObj(), 2 )
vs.SetPenFore( vs.LNewObj(), 65535, 0, 0 )
vs.SetFPat( vs.LNewObj(), 0 )
b1, b2 = vs.GetBBox( vs.LNewObj() )
```

## See Also
VS Functions:
* [GetTextVerticalAlign](GetTextVerticalAlign.md) | [SetTextVertAlignN](SetTextVertAlignN.md)
* [GetTextJust](GetTextJust.md) | [SetTextJust](SetTextJust.md) | [SetTextJustN](SetTextJustN.md)

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
