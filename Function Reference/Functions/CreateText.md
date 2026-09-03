# CreateText

## Description
Procedure CreateText creates a new text object in a VectorWorks document. The text object is created using the current pen position and default attributes.

```pascal
PROCEDURE CreateText(theText : DYNARRAY[] of CHAR);
```

```python
def vs.CreateText(theText):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|DYNARRAY[] of CHAR|Text string.|

## Remarks
*\_c\_*, 2015.12.19: If you draw text, it is important to have a proper text size on the document or you'll see the error "An incorrect object is described".
```pascal
PushAttrs;
	NameClass(ClassList(1));
	PenPat(1);
	FillPat(0);
	PenFore(0, 0, 0);
	TextSize(9); { avoid accidental small text size rising the error "An incorrect object is described" }
	CreateText('Text');
PopAttrs;
```

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
    Txt   :ARRAY [1..100] of STRING;
    Outpt :DYNARRAY[] of CHAR;
    i     :INTEGER;
BEGIN
    FOR i := 1 TO 5 DO txt[i] := 'asdf';
    i := 2;
    Outpt := Txt[1];
    WHILE Txt[i] <> '' DO BEGIN
        OutPt := Concat(Outpt, Chr(13), Txt[i]);
        i := i + 1;
    END;
    Layer('Text');
    CreateText(Outpt);
    Layer('Layer-1');
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	txt = []
	for i in range(0,4):
		txt.append('asdf')
	txt.append("")
	i = 1
	Outpt = txt[0]
	while txt[i] != "":
		OutPt = vs.Concat(Outpt, vs.Chr(13), txt[i])
		i = i + 1
		
	vs.Layer('Text')
	vs.CreateText(Outpt)
	vs.Layer('Layer-1')

Example()
```

```pascal
IF Ang2BearingStr(tmpAngle) <> GetText (PickObject (ptX + tmpVector[1] + labelVector[1], ptY + tmpVector[2] + labelVector[2])) THEN
	CreateText(Ang2BearingStr(tmpAngle));

BEGIN
	TextOrigin(0,0);
	CreateText(Errors);
END;

BSB := SetObjEndMarker(LNewObj,0,30,.1,0,2,2,(pArrows <> kCSStrDown));
SetFPat(LNewObj,0);
angle:=angle*PI/(2*180);
Moveto(Sin(angle)*rad,cos(angle)*rad);
CreateText(anno);
SetTextJust(LNewObj,2);
SetTextVerticalAlign(LNewObj,3);
setfpat(lnewobj,GetFPat(parmHand));
GetFillBack(parmHand,red,grn,bl);
```
```python
vs.MoveTo ( textPtx, textPty )
vs.DSelectAll()
vs.CreateText( vs.PSheet_No )
vs.SetFPat( vs.LNewObj(), 0 )
vs.Rotate( dTextRotation )

vs.Absolute()
vs.MoveTo( 0, 0 )
vs.BeginGroup()
vs.CreateText( message1 )
vs.SetTextVerticalAlign( vs.LNewObj(), 3 )
vs.SetTextJust( vs.LNewObj(), 2 )
vs.SetPenFore( vs.LNewObj(), 65535, 0, 0 )
vs.SetFPat( vs.LNewObj(), 0 )
```
See also in tutorials: [02. Draw 2D Geometry Primitives](ai%20examples/02_Draw2DPrimitives.md), [07. Set Up Document Structure: Layers and Classes](ai%20examples/07_LayersAndClasses.md), [08. Attach and Read Records on Objects](ai%20examples/08_AttachAndReadRecords.md), [09. Dimensioning and Text Annotation](ai%20examples/09_DimensionsAndText.md)

## See Also
VS Functions:
[BeginText](BeginText.md) 
| [EndText](EndText.md)

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
