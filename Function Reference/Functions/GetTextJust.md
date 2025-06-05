# GetTextJust

## Description
Function GetTextJust returns the text justification of the referenced text object.


![Text Locus](files/Textlocus.gif)

**Table - Text Justification**

| Justification | Constant |
|---------------|----------|
| Left          | 1        |
| Center        | 2        |
| Right         | 3        |
| Justify       | 4        |

```pascal
FUNCTION GetTextJust(TextHd : HANDLE): INTEGER;
```

```python
def vs.GetTextJust(TextHd):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|TextHd|HANDLE|Handle to text object.|

## Remarks
([[User:Orso.b.schmid|Orso]], 2012 Mai. 26): The constant 4 "Justify" is introduced by VW 2011.

## See Also
VS Functions:
* [SetTextJust](SetTextJust.md) | [SetTextJustN](SetTextJustN.md) 
* [GetTextVerticalAlign](GetTextVerticalAlign.md) | [SetTextVerticalAlign](SetTextVerticalAlign.md)

## Version
Availability: from MiniCAD 6.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
