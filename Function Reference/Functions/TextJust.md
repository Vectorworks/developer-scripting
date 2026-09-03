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

## Examples
```pascal
	tmpAngle := 180 + tmpAngle
else if ((tmpAngle <= 180) AND (tmpAngle > 90)) THEN
	tmpAngle := tmpAngle - 180;
TextRotate(tmpAngle);
TextJust(2);
TextOrigin(ptX + tmpVector[1] + labelVector[1], ptY + tmpVector[2] + labelVector[2]);

planrotation := GetPref(92);
SetPref(92, FALSE);
PushAttrs;
GetOrigin(PX, PY);
TextJust (1);
TextVerticalAlign (1);
TextSize (kTextSize);
boxSize := kBoxSize * getUPI * GetLScale (ActLayer);
textdX := kTextdX * getUPI * GetLScale (ActLayer);

TextJust(1);
TextVerticalAlign(3);
textTextSize := TextScale * str2num(pTSize);
labelTextSize := textTextSize * pLFact;
```
```python
vs.TextVerticalAlign(3)
vs.TextJust(2)
```

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
