# BeginMXtrd

## Description
Procedure BeginMXtrd creates a multiple extrude object in a VectorWorks document. BeginMXtrd uses 2D object creation procedure calls to define the &quot;template&quot; for the object.

You should call EndMXtrd after the object creation procedures to complete the definition and generate the object in the document.

A multiple extrude object is a 3D object created from three or more 2D objects, which are used as defining shapes for the extruded object.

```pascal
PROCEDURE BeginMXtrd(
				startDistance : REAL;
				endDistance   : REAL);
```

```python
def vs.BeginMXtrd(startDistance, endDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|startDistance|REAL|Start distance from document ground plane.|
|endDistance|REAL|End distance from document ground plane.|

## Examples
#### VectorScript ####
```pascal
BeginMXtrd(0',1 363/512&quot;);
Rect(-125/128&quot;,1 113/512&quot;,375/512&quot;,375/512&quot;);
Rect(-25/32&quot;,1 113/512&quot;,275/512&quot;,375/512&quot;);
Rect(-75/128&quot;,1 113/512&quot;,325/1024&quot;,375/512&quot;);
Locus(-275/2048&quot;,125/128&quot;);
Rect(-75/128&quot;,1 113/512&quot;,325/1024&quot;,375/512&quot;);
Rect(-25/32&quot;,1 113/512&quot;,275/512&quot;,375/512&quot;);
Rect(-125/128&quot;,1 113/512&quot;,375/512&quot;,375/512&quot;);
EndMXtrd;
```
#### Python ####
```python
vs.BeginMXtrd(0,1 + 363/512)
vs.Rect(-125/128,1 + 113/512,375/512,375/512)
vs.Rect(-25/32,1 + 113/512,275/512,375/512)
vs.Rect(-75/128,1 + 113/512,325/1024,375/512)
vs.Locus(-275/2048,125/128)
vs.Rect(-75/128,1 + 113/512,325/1024,375/512)
vs.Rect(-25/32,1 + 113/512,275/512,375/512)
vs.Rect(-125/128,1 + 113/512,375/512,375/512)
vs.EndMXtrd()
```

```pascal
BeginMXtrd(0,RailThick);
IF Arch = 4 THEN
	BEGIN
	BeginPoly;
	PolyArc(X1,Ext,Y2,RHeight,RLength,0,Arch,TRUE);

BeginMxtrd(cHeight+cRoof_Thickness,cHeight+cRoof_Thickness+cRise);
	Rect(-(cWidth/2+cOverhang),-(cWidth/2+cOverhang),(cWidth/2+cOverhang),(cWidth/2+cOverhang));
	Locus(0.0,0.0);
EndMxtrd;
SetTextureRef(lNewObj,-1,3);

   r1 := LegThick * (100 - gPLeg_Taper_Pcent)/100;
ChangeToClass(TableLegsCName);
{ create table legs }
   FOR i := 1 TO 4 DO BEGIN
       BeginMXtrd(0, THeight - TopThick);
           IF PLeg_Shape = kTCLegShapeSquare THEN BEGIN
			{ bottom of tapered leg. -gCon/3 offsets leg from skirt slightly }
               Rect(-gCon/3, -gCon/3, r1 - gCon/3, r1 - gCon/3);
			{ leg offset if necessary }
```
```python
# Curbs
vs.BeginMXtrd( 0, length )
vs.BeginPoly()
vs.AddPoint( p1 )
vs.AddPoint( p2 )
vs.AddPoint( p3 )
```

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
