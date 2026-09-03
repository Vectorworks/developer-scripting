# SetTextWidth

## Description
Procedure SetTextWidth Sets the text wrapping margin width of the referenced text object.   

A call to SetTextWidth automatically activates text wrapping.

```pascal
PROCEDURE SetTextWidth(
				theText       : HANDLE;
				widthDistance : REAL);
```

```python
def vs.SetTextWidth(theText, widthDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|
|widthDistance|REAL|Text wrapping margin setting for text.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;

FUNCTION IncreaseTextWidth(h :HANDLE) :BOOLEAN;
BEGIN
SetTextWidth(h, GetTextWidth(h) * 1.2);
END;

BEGIN
ForEachObjectInLayer(IncreaseTextWidth, 2, 0, 4);
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
	CreateText(pText);
	SetTextVerticalAlign(LNewObj, 3);
	SetTextJust(LNewObj, 2);
	GetContainerInfo(objHand, containerHandle, containerType, containerScale);
	SetTextWidth(LNewObj, pText_Width * containerScale);
END;

	TextOrigin(0, textCenterY * Scale);
	CreateText(pText);
	h := LNewObj;
	SetTextJust(h, 2);
	SetTextWidth(h, TextBoxWidth * Scale);
	SetTextVerticalAlign(h, 3);
	SetFPat(h, 0);
END;

	CreateText(strBelow);
h2 := LNewObj;
SetFPat(h1,0);
SetFPat(h2,0);
SetTextWidth(h2,(gScaleFactor*wid));
```
```python
vs.SetTextWidth('Example', 1.0)
```

## See Also
VS Functions:
[GetTextWidth](GetTextWidth.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
