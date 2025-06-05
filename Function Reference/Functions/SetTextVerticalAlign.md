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

## See Also
VS Functions:
* [GetTextVerticalAlign](GetTextVerticalAlign.md) | [SetTextVertAlignN](SetTextVertAlignN.md)
* [GetTextJust](GetTextJust.md) | [SetTextJust](SetTextJust.md) | [SetTextJustN](SetTextJustN.md)

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
