# SetTextJustN

## Description
Procedure SetTextJustN sets the text justification of the referenced text object without changing its location.

![Text Locus](files/Textlocus.gif)

**Table - Text Justification**

| Justification | Constant |
|---------------|----------|
| Left          | 1        |
| Center        | 2        |
| Right         | 3        |
| Justify       | 4        |

```pascal
PROCEDURE SetTextJustN(
				TextHd   : HANDLE;
				JustFlag : INTEGER);
```

```python
def vs.SetTextJustN(TextHd, JustFlag):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|TextHd|HANDLE|Handle to text object.|
|JustFlag|INTEGER|Justification setting for text.|

## Remarks
([[User:Orso.b.schmid|Orso]], 2012 Mai. 26): The constant 4 "Justify" is introduced by VW 2011

## Examples
```pascal
TextOrigin(0,0);
IF text<>'' THEN CreateText(text) ELSE CreateText(' ');
{Set correct text alignment}
SetTextVertAlignN(LNewObj, tVAlign);
SetTextJustN(LNewObj, tJust);
SetTextSpace(LNewObj, 2);
SetFPat(LNewObj,0);
GetTextOrientation(LNewObj, ptX, ptY, angle, isMirrored);
{Move the text object at the correct location}

BEGIN
	SetTextJustN(labelText,2);
	LabelOffsetY := (19*UPI) - labelNumber * (6 * UPI);
	SetTextOrientation( labelText, (kLegendLabelLoc * UPI), LabelOffsetY, 0, FALSE );
END;

BEGIN
	SetTextJustN(HanToText, 2);
END;
```
```python
import vs

# Procedure SetTextJustN sets the text justification of the referenced text
# object without changing its location.
TextHd = vs.FSActLayer()  # handle to the first selected object on the active layer
JustFlag = 1

vs.SetTextJustN(TextHd, JustFlag)
```

## See Also
VS Functions:
[GetTextJust](GetTextJust.md) | [SetTextJust](SetTextJust.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
