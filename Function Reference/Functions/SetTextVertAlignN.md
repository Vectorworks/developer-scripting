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

## See Also
VS Functions:
* [GetTextVerticalAlign](GetTextVerticalAlign.md) | [SetTextVerticalAlign](SetTextVerticalAlign.md)
* [GetTextJust](GetTextJust.md) | [SetTextJust](SetTextJust.md) | [SetTextJustN](SetTextJustN.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
