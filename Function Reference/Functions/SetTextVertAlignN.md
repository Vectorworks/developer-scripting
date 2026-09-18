# SetTextVertAlignN

## Description
Procedure SetTextVertAlignN sets the vertical alignment of the referenced text object without changing its location.

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
PROCEDURE SetTextVertAlignN(
				TextHd            : HANDLE;
				verticalAlignment : INTEGER);
```

```python
def vs.SetTextVertAlignN(TextHd, verticalAlignment):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|TextHd|HANDLE|Handle to the text object.|
|verticalAlignment|INTEGER|Vertical alignment setting for text.|

## Examples
```pascal
TextJust(tJust);
TextOrigin(0,0);
IF text<>'' THEN CreateText(text) ELSE CreateText(' ');
{Set correct text alignment}
SetTextVertAlignN(LNewObj, tVAlign);
SetTextJustN(LNewObj, tJust);
SetTextSpace(LNewObj, 2);
SetFPat(LNewObj,0);
GetTextOrientation(LNewObj, ptX, ptY, angle, isMirrored);

	Rect( x1+x, y1+y, x2+x, y2+y );
	HRotate( LNewObj, x, y, rot );
	CreateText(GetPluginString(8022));
	SetTextJustN(LNewObj, 2 );
	SetTextVertAlignN(LNewObj, 3 );
	SetTextOrientation( LNewObj, x + (x1 + x2)/2, y + (y1+y2)/2, 0, FALSE );
	HRotate( LNewObj, x, y, rot );
	SetTextSize(LNewObj, 0, GetTextLength(LNewObj), (72 / 25.4) * ( Abs( x1 - x2 ) + Abs( y1 - y2 ) ) / GetLScale(ActLayer));
EndGroup;
```
```python
import vs

# Procedure SetTextVertAlignN sets the vertical alignment of the referenced
# text object without changing its location.
TextHd = vs.FSActLayer()  # handle to the first selected object on the active layer
verticalAlignment = 1

vs.SetTextVertAlignN(TextHd, verticalAlignment)
```

## See Also
VS Functions:
* [GetTextVerticalAlign](GetTextVerticalAlign.md) | [SetTextVerticalAlign](SetTextVerticalAlign.md)
* [GetTextJust](GetTextJust.md) | [SetTextJust](SetTextJust.md) | [SetTextJustN](SetTextJustN.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
