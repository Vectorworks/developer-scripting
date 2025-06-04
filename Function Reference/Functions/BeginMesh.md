# BeginMesh

## Description
Procedure BeginMesh begins the efinition of a 3D mesh object in VectorWorks. Any 3D point or planar object call after BeginMesh will be included in the mesh object. 

A mesh object allows the user to select and manipulate each vertex within its wire-frame model.

```pascal
PROCEDURE BeginMesh;
```

```python
def vs.BeginMesh():
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
Poly3D(0',0',4' 0",4' 0",0',4' 0",4' 0",-4' 0",4' 0",0',-4' 0",4' 0");
Smooth(0);
Poly3D(0',0',0',4' 0",0',0',4' 0",-4' 0",0',0',-4' 0",0');
Smooth(0);
Poly3D(0',-4' 0",0',0',-4' 0",4' 0",0',0',4' 0",0',0',0');
Poly3D(4' 0",-4' 0",0',4' 0",-4' 0",4' 0",0',-4' 0",4' 0",0',-4' 0",0');
Poly3D(4' 0",0',0',4' 0",0',4' 0",4' 0",-4' 0",4' 0",4' 0",-4' 0",0');
Poly3D(0',0',0',0',0',4' 0",4' 0",0',4' 0",4' 0",0',0');
EndMesh;
```
#### Python ####
```python
vs.BeginMesh()
vs.ClosePoly()
vs.PenSize(1)
vs.PenPat(2)
vs.FillPat(0)
vs.Poly3D(0, 0, 4*12, 4*12, 0, 4*12, 4*12, -4*12, 4*12, 0, -4*12, 4*12)
vs.Smooth(0)
vs.Poly3D(0*12,0*12,0*12,4*12 ,0*12,0*12,4*12 ,-4*12 ,0*12,0*12,-4*12 ,0*12)
vs.Smooth(0)
vs.Poly3D(0*12,-4*12 ,0*12,0*12,-4*12 ,4*12 ,0*12,0*12,4*12 ,0*12,0*12,0*12)
vs.Poly3D(4*12 ,-4*12 ,0*12,4*12 ,-4*12 ,4*12 ,0*12,-4*12 ,4*12 ,0*12,-4*12 ,0*12)
vs.Poly3D(4*12 ,0*12,0*12,4*12 ,0*12,4*12 ,4*12 ,-4*12 ,4*12 ,4*12 ,-4*12 ,0*12)
vs.Poly3D(0*12,0*12,0*12,0*12,0*12,4*12 ,4*12 ,0*12,4*12 ,4*12 ,0*12,0*12)
vs.EndMesh()
```

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
