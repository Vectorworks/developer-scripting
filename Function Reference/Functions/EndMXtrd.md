# EndMXtrd

## Description
Procedure EndMXtrd completes the definition of a multiple extrude object within a VectorWorks document. On calling EndMXtrd, the object is created in the document from the preceding object creation calls.

It is recommended to call ResetOrientation3D after 3D object creations in order to ensure that the new 3D objects will draw properly.

```pascal
PROCEDURE EndMXtrd;
```

```python
def vs.EndMXtrd():
    return None
```

## Examples
==== VectorScript ====
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
==== Python ====
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
