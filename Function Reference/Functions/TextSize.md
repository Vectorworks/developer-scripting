# TextSize

## Description
Procedure TextSize sets the active text size of a VectorWorks document.

Text size is specified in points (1 point = 1/72&quot;). If 0 is specified, then the font size will default to 12 pt text.

```pascal
PROCEDURE TextSize(size : REAL);
```

```python
def vs.TextSize(size):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|size|REAL|Point size of text.|

## Remarks
The size parameter is now a REAL so fractional point sizes can be specified. This should be fully compatible with existing VectorScript code. [9/14/98 - PCP] 

Text size is in page-space and does not take drawing scale into account.  [9/14/98 - PCP]

## Examples
#### VectorScript ####
```pascal
TextSize(18);
{set the active text size to 18 point}
```
#### Python ####
```python

```

```pascal
PushAttrs;
GetOrigin(PX, PY);
TextJust (1);
TextVerticalAlign (1);
TextSize (kTextSize);
boxSize := kBoxSize * getUPI * GetLScale (ActLayer);
textdX := kTextdX * getUPI * GetLScale (ActLayer);
textdy := ktextdy * getUPI * GetLScale (ActLayer);
SetCursor(WatchC);

BEGIN
	TextSize(txtSize);
	CASE textStyleIndex OF
		1: TextFace([Bold]);
		2: TextFace([Italic]);
		3: TextFace([Bold,Italic]);

BEGIN
gVAlign := GetPrefInt(83);
SetPrefInt(83, tVAlign);
TextSize(Str2Num(tSize));
TextJust(tJust);
TextOrigin(0,0);
IF text<>'' THEN CreateText(text) ELSE CreateText(' ');
{Set correct text alignment}
```
```python
vs.TextSize(1.0)
```
See also in tutorials: [09. Dimensioning and Text Annotation](ai%20examples/09_DimensionsAndText.md)

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
