# GetTextWrap

## Description
Procedure GetTextWrap returns the text wrap mode of the referenced text object.

```pascal
FUNCTION GetTextWrap(theText : HANDLE): BOOLEAN;
```

```python
def vs.GetTextWrap(theText):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|

## Examples
```pascal
MyStyle := GetTextStyle(HanToLegendText, 0);
MyTextJust := GetTextJust(HanToLegendText);
MyVertAlign := GetTextVerticalAlign(HanToLegendText);
MyTextWidth := GetTextWidth(HanToLegendText);
MyTextWrap := GetTextWrap(HanToLegendText);
GetPenFore(HanToLegendText, MyPFRColor, MyPFGColor, MyPFBColor);
GetPenBack(HanToLegendText, MyPBRColor, MyPBGColor, MyPBBColor);
GetTextOrientation(HanToLegendText, MyTextX, MyTextY, MyTextAng, MyTextMirror);
MyTextFPat := GetFPat(HanToLegendText);
```
```python
import vs

# Procedure GetTextWrap returns the text wrap mode of the referenced text object.
theText = 'Example text'

ok = vs.GetTextWrap(theText)
if ok:
    vs.Message('GetTextWrap succeeded')
else:
    vs.Message('GetTextWrap failed')
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
