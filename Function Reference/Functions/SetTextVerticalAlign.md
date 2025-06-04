# SetTextVerticalAlign

## Description
Procedure SetTextVerticalAlign sets the vertical alignment of the referenced text object. 


![Text Locus](files/Textlocus.gif)

{| class="wikitable_c"
! Justification !! Constant
|+ Table - Text Vertical Justification
|-
| Top of text box 
| style="text-align:center"| 1
|-
| Top baseline 
| style="text-align:center"| 2
|-
| Text centerline 
| style="text-align:center"| 3
|-
| Bottom baseline 
| style="text-align:center"| 4
|-
| Bottom of text box 
| style="text-align:center"| 5
|}

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
([[User:Orso.b.schmid|Orso]], 2012 Mai. 27): This routine needs a screen redraw after running. The text object will shift after changing the alignment, use [[VS:SetTextVertAlignN]] if the shift is not wished.

## See Also
VS Functions:
* [GetTextVerticalAlign](GetTextVerticalAlign.md) | [SetTextVertAlignN](SetTextVertAlignN.md)
* [GetTextJust](GetTextJust.md) | [SetTextJust](SetTextJust.md) | [SetTextJustN](SetTextJustN.md)

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
