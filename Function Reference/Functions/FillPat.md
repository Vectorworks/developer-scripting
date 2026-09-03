# FillPat

## Description
Procedure FillPat sets the active fill pattern for the document. Any objects created after a calling this procedure will use the specified fill pattern.

Fill patterns and their associated constants can be found in the [VectorScript Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#fill-patterns).

```pascal
PROCEDURE FillPat(patNumber : LONGINT);
```

```python
def vs.FillPat(patNumber):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|patNumber|LONGINT|Index of fill pattern to be set as document default.|

## Examples
#### VectorScript ####
```pascal
Rect(0,0,2,2);
FillPat(21);
Rect(2,2,4,4);
```
#### Python ####
```python
vs.Rect(0,0,2,2)
vs.FillPat(21)
vs.Rect(2,2,4,4)
```

```pascal
BEGIN
	pushattrs;
	fillpat(1);
	fillback(65535,42000,0);
	BeginMXtrd(0.0,cWidth/3);
		Oval(-cWidth/6,-cWidth/6,cWidth/6,cWidth/6);
		Oval(-cWidth/6,-cWidth/6,cWidth/6,cWidth/6);

pushattrs;
IF pAngle<360 THEN angle:= pAngle
ELSE angle:= 359;
rad:= cOuter_Radius-cWidth/2;
FillPat(0);

TextRotate (#0);
TextSpace (2);
TextJust (2);
TextVerticalAlign (3);
FillPat (kFPat0);
```
```python
vs.FillPat(0)
hDuplicated = vs.CreateDuplicateObject( hObjectHand, gObjHandle )

if not vs.IsFPatByClass( objHand ):
	penPat	= vs.GetFPat( objHand )
	vs.FillPat( penPat )
```
See also in tutorials: [02. Draw 2D Geometry Primitives](ai%20examples/02_Draw2DPrimitives.md)

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
