# EndMesh

## Description
Procedure EndMesh completes the definition of a mesh object within a VectorWorks document. On calling EndMesh, the mesh is created in the document from the preceding object creation calls.

It is recommended to call ResetOrientation3D after 3D object creations in order to ensure that the new 3D objects will draw properly.

```pascal
PROCEDURE EndMesh;
```

```python
def vs.EndMesh():
    return None
```

## Examples
#### VectorScript ####
```pascal
BeginMesh;
ClosePoly;
PenSize(1);
PenPat(2);
FillPat(0);
Poly3D(0',0',4'-0&quot;,4'-0&quot;,0',4'-0&quot;,4'-0&quot;,-4'-0&quot;,4'-0&quot;,0',-4'-0&quot;,4'-0&quot;);
Smooth(0);
Poly3D(0',0',0',4'-0&quot;,0',0',4'-0&quot;,-4'-0&quot;,0',0',-4'-0&quot;,0');
Smooth(0);
Poly3D(0',-4'-0&quot;,0',0',-4'-0&quot;,4'-0&quot;,0',0',4'-0&quot;,0',0',0');
Poly3D(4'-0&quot;,-4'-0&quot;,0',4'-0&quot;,-4'-0&quot;,4'-0&quot;,0',-4'-0&quot;,4'-0&quot;,0',-4'-0&quot;,0');
Poly3D(4'-0&quot;,0',0',4'-0&quot;,0',4'-0&quot;,4'-0&quot;,-4'-0&quot;,4'-0&quot;,4'-0&quot;,-4'-0&quot;,0');
Poly3D(0',0',0',0',0',4'-0&quot;,4'-0&quot;,0',4'-0&quot;,4'-0&quot;,0',0');
EndMesh;
```
#### Python ####
```python
vs.BeginMesh()
vs.ClosePoly()
vs.PenSize(1)
vs.PenPat(2)
vs.FillPat(0)
vs.Poly3D(0,0,4*12,4*12,0*12,4*12,4*12,-4*12,4*12,0,-4*12,4*12)
vs.Smooth(0)
vs.Poly3D(0,0,0,4*12,0,0,4*12,-4*12,0,0,-4*12,0)
vs.Smooth(0)
vs.Poly3D(0,-4*12,0,0,-4*12,4*12,0,0,4*12,0,0,0)
vs.Poly3D(4*12,-4*12,0,4*12,-4*12,4*12,0,-4*12,4*12,0,-4*12,0)
vs.Poly3D(4*12,0,0,4*12,0,4*12,4*12,-4*12,4*12,4*12,-4*12,0)
vs.Poly3D(0,0,0,0,0,4*12,4*12,0,4*12,4*12,0,0)
vs.EndMesh()
```

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
