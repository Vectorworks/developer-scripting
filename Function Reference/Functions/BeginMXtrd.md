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

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
