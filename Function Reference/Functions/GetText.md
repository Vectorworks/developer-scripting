# GetText

## Description
Function GetText returns the text contained within the referenced text object.

```pascal
FUNCTION GetText(objectHd : HANDLE): DYNARRAY[] of CHAR;
```

```python
def vs.GetText(objectHd):
    return DYNARRAY[] of CHAR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to text object.|

## Examples
```pascal
IF Ang2BearingStr(tmpAngle) <> GetText (PickObject (ptX + tmpVector[1] + labelVector[1], ptY + tmpVector[2] + labelVector[2])) THEN
	CreateText(Ang2BearingStr(tmpAngle));

{parse the hole txtFoundH string in order to separate the KN No. from the rest and thus get its full prefix and suffix}
if ok then BEGIN
	{find the start and end position of the prefix-No.-suffix string in  the text.}
	temppos := Pos( noteNostr, GetText( H ) );
	{check whether the temppos is not 0, i.e. whether the keynote pref-num-suff is not in the text's object text at all}
	{if so - use the text's object text as a prefix! followed by ' '}
	if ( tempPos = 0 ) THEN BEGIN
		KNprefix := Concat( GetText( H ), ' ', KNprefix);

str := gettext(textHandle);
IF NOT(pLabel) THEN
	settextstyle(texthandle,0,pos2,textStyleindex)
	{settextstyle(texthandle,0,textLength,textStyleindex)}
```
```python
import vs

# Function GetText returns the text contained within the referenced text object.
objectHd = vs.FSActLayer()  # handle to the first selected object on the active layer

text = vs.GetText(objectHd)
vs.Message('GetText returned: ' + str(text))
```

## See Also
VS Functions:
[SetText](SetText.md)

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
