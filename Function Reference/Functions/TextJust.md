# TextJust

## Description
Procedure TextJust sets the active text justification for a VectorWorks document. 

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
PROCEDURE TextJust(justify : INTEGER);
```

```python
def vs.TextJust(justify):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|justify|INTEGER|Justification setting for document.|

## Remarks
There doesn't seem to be a way to get the document DEFAULT text justification like FUNCTION GetDefaultTextJust : INTEGER;

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
