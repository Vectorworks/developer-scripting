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

## See Also
VS Functions:
[GetTextJust](GetTextJust.md) | [SetTextJust](SetTextJust.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
