# SetTextWrap

## Description
Procedure SetTextWrap sets the text wrap mode of the referenced text object.

```pascal
PROCEDURE SetTextWrap(
				theText : HANDLE;
				wrap    : BOOLEAN);
```

```python
def vs.SetTextWrap(theText, wrap):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|
|wrap|BOOLEAN|Text wrap setting for text.|

## Remarks
If this is set to false, it will cause the margin width to be recomputed and the text block to be reformatted. If it is set to true, the width remains the same, and text will be wrapped to fit the current margin. Use SetTextWidth to change the margin.
By default, text is created with wrapping set to false.

## Examples
```pascal
	SetPenFore (LNewObj, 45000, 0, 0);
	TextJust (2);
	TextOrigin (-width/2, height/2);
	CreateText (errMsg);
	SetTextWrap (LNewObj, TRUE);
	SetTextWidth (LNewObj, width - .12");
	SetTextSize (LNewObj, 0, Len (errMsg), 12/gTitleBlockScale);
	SetPenFore (LNewObj, 45000, 0, 0);
EndGroup;

SetTextStyle(HanToText, 0, Len(GetText(HanToText)), MyStyle);
SetTextJust(HanToText, MyTextJust);
SetTextVerticalAlign(HanToText, MyVertAlign);
SetTextWidth(HanToText, MyTextWidth);
SetTextWrap(HanToText, MyTextWrap);
SetPenFore(HanToText, MyPFRColor, MyPFGColor, MyPFBColor);
SetPenBack(HanToText, MyPBRColor, MyPBGColor, MyPBBColor);
SetFPat(HanToText, MyTextFPat);
SetFillFore(HanToText, MYFFRColor, MyFFGColor, MyFFBColor);
```
```python
import vs

# Procedure SetTextWrap sets the text wrap mode of the referenced text object.
theText = 'Example text'
wrap = True

vs.SetTextWrap(theText, wrap)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
