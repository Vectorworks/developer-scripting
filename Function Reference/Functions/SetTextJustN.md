# SetTextJustN

## Description
Procedure SetTextJustN sets the text justification of the referenced text object without changing its location.

![Text Locus](files/Textlocus.gif)

{| class="wikitable_c"
|+ Table - Text Justification
! Justification !! Constant
|- 
| Left
| style="text-align:center"| 1
|- 
| Center
| style="text-align:center"| 2
|-
| Right
| style="text-align:center"| 3
|-
| Justify
| style="text-align:center"| 4
|}

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

## See Also
VS Functions:
[GetTextJust](GetTextJust.md) | [SetTextJust](SetTextJust.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
