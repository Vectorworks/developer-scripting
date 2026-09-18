# SetTextAdorner

## Description
This function creates a relationship between the specified text block and the text adorner such that when theText Block is scaled in a VP, the text adorner is also scaled. Several objects can be adorned to the same text object.

```pascal
FUNCTION SetTextAdorner(
				textBlock   : HANDLE;
				textAdorner : HANDLE;
				p           : REAL): Boolean;
```

```python
def vs.SetTextAdorner(textBlock, textAdorner, p):
    return Boolean
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textBlock|HANDLE|The Text object being adorned.|
|textAdorner|HANDLE|The object used to adorn the specified text.|
|p|REAL|The point by which texts will be scaled.|

## Examples
```pascal
PROCEDURE Example;
VAR
theText      :HANDLE;
theShape : HANDLE;
restult :      BOOLEAN;
BEGIN
TextVerticalAlign(3);
TextJust(2);
MoveTo(0,0);
RectangleN(-.5&quot;,      -.5&quot;, 1, 0, 1&quot;, 1&quot;);
theShape :=      lNewObj;
CreateText('ID1');
theText :=      lNewObj;
restult :=      SetTextAdorner(theText,theShape,0,0);
END;
RUN(Example);
```

```pascal
IF hText1 <> NIL THEN result := SetTextAdorner(hText1,hBox,x1-margin,y1+margin);
IF hText2 <> NIL THEN result := SetTextAdorner(hText2,hBox,x1-margin,y1+margin);
IF hText3 <> NIL THEN result := SetTextAdorner(hText3,hBox,x1-margin,y1+margin);
IF hText4 <> NIL THEN result := SetTextAdorner(hText4,hBox,x1-margin,y1+margin);
IF hText5 <> NIL THEN result := SetTextAdorner(hText5,hBox,x1-margin,y1+margin);

BEGIN
	SetPlanarRef( h, 0 );
	result := SetTextAdorner(TextHand,h,TextLocX,TextLocY);
	IF GetPref(16) THEN
		BEGIN
		WhiteR := 0;
		WhiteG := 0;

			RectangleN( 0, -SizeFactor/2, 1, 0, bubble_width, SizeFactor )
		END;
	END; {of CASE}
hBubble := LNewObj;
return := SetTextAdorner(title_h,hBubble,SizeFactor/2,0);
END;
```
```python
import vs

# This function creates a relationship between the specified text block and
# the text adorner such that when theText Block is scaled in a VP, the text
# adorner i.
textBlock = vs.FSActLayer()  # handle to the first selected object on the active layer
textAdorner = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
p = 1.0

ok = vs.SetTextAdorner(textBlock, textAdorner, p)
if ok:
    vs.Message('SetTextAdorner succeeded')
else:
    vs.Message('SetTextAdorner failed')
```

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
