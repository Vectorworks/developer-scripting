# GetTextVerticalAlign

## Description
Function GetTextVerticalAlign returns the vertical alignment of the referenced text object.


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
FUNCTION GetTextVerticalAlign(TextHd : HANDLE): INTEGER;
```

```python
def vs.GetTextVerticalAlign(TextHd):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|TextHd|HANDLE|Handle to text object.|

## See Also
VS Functions:
* [SetTextVerticalAlign](SetTextVerticalAlign.md) | [SetTextVertAlignN](SetTextVertAlignN.md)
* [GetTextJust](GetTextJust.md) | [SetTextJust](SetTextJust.md) | [SetTextJustN](SetTextJustN.md)

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
