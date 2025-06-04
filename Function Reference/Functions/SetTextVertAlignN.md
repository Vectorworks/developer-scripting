# SetTextVertAlignN

## Description
Procedure SetTextVertAlignN sets the vertical alignment of the referenced text object without changing its location.

[[Image:textlocus.gif| left]]

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

## See Also
VS Functions:
* [GetTextVerticalAlign](GetTextVerticalAlign.md) | [SetTextVerticalAlign](SetTextVerticalAlign.md)
* [GetTextJust](GetTextJust.md) | [SetTextJust](SetTextJust.md) | [SetTextJustN](SetTextJustN.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
