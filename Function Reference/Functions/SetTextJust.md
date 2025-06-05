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
([[User:Orso.b.schmid|Orso]], 2012 Mai. 26): The constant 4 "Justify" is introduced by VW 2011. This routine needs a screen redraw after running. The text object will shift after changing the alignment, use [[VS:SetTextJustN]] if the shift is not wished.

## See Also
VS Functions:
* [GetTextJust](GetTextJust.md) | [SetTextJustN](SetTextJustN.md) 
* [GetTextVerticalAlign](GetTextVerticalAlign.md) | [SetTextVerticalAlign](SetTextVerticalAlign.md)

## Version
Availability: from MiniCAD 6.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
