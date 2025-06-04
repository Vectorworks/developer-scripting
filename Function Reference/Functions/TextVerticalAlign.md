# TextVerticalAlign

## Description
Procedure TextVerticalAlign sets the active text vertical alignment of a VectorWorks document. 




{| class="wikitable_c"
|+ Table - Text Vertical Justification
! Justification !! Constant
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

![Text Locus](files/Textlocus.gif)

```pascal
PROCEDURE TextVerticalAlign(verticalAlignment : INTEGER);
```

```python
def vs.TextVerticalAlign(verticalAlignment):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|verticalAlignment|INTEGER|Vertical alignment setting for document.|

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
