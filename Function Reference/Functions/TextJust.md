# TextJust

## Description
Procedure TextJust sets the active text justification for a VectorWorks document. 

![Text Locus](files/Textlocus.gif)

**Table - Text Justification**

| Justification | Constant |
|---------------|----------|
| Left          | 1        |
| Center        | 2        |
| Right         | 3        |
| Justify       | 4        |

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
