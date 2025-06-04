# SetText

## Description
Procedure SetText sets the content of the referenced text object. The new text is assigned the font, size and style characteristics of the first character of the old text string.

```pascal
PROCEDURE SetText(
				objectHd : HANDLE;
				text     : DYNARRAY[] of CHAR);
```

```python
def vs.SetText(objectHd, text):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to text object.|
|text|DYNARRAY[] of CHAR|New text string value.|

## Examples
==== VectorScript ====
```pascal
SetText(hText,'A new text string value');
```
Better example:
```pascal
PROCEDURE Example;
{ (c) Petri Sakkinen 1997 or thereabouts } 
VAR
theText, theRest :HANDLE;
x, y :REAL; 
textstart, moretext :STRING;
BEGIN
theText := FSActLayer;
Message('Point text blocks to be concatenated');
textstart := GetText(theText);
GetPt(x, y);
theRest := PickObject(x, y);
REPEAT
moretext := GetText(theRest);
textstart := Concat(textstart, ' ', moretext);
DelObject(theRest);
GetPt(x, y);
theRest := PickObject(x, y);
UNTIL (theRest = NIL);
SetText(theText, textstart);
ClrMessage;
END;
RUN(Example);
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
