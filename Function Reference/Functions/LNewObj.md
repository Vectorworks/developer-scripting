# LNewObj

## Description
Returns a handle to the last object created by a VectorScript function call during the current script execution.

```pascal
FUNCTION LNewObj : HANDLE;
```

```python
def vs.LNewObj():
    return HANDLE
```

## Remarks
[As of 8.0.0b10]

If the object has been deleted since it was created, this function returns NIL. It is recommended that you call LNewObj immediately after the function or procedure which created the object to avoid problems.

## Examples
```pascal
resultH := LNewObj;
```
```python
vs.MoveTo ( textPtx, textPty )
vs.DSelectAll()
vs.CreateText( vs.PSheet_No )
vs.SetFPat( vs.LNewObj(), 0 )
vs.Rotate( dTextRotation )

vs.Locus((vs.PRadius+vs.PCurb_Width+(vs.PWidth/2)),0); SetAttrsByClassOrParent( vs.LNewObj(), gObjHandle, gCurb_Class )
vs.EndSweep()

vs.AddPoint( p6 )
vs.AddPoint( p5 )
vs.EndPoly()
SetAttrsByClassOrParent(vs.LNewObj(), gObjHandle, gPaving_Class, vs.PShow_Joints)
```
See also in tutorials: [01. Draw a Room with Walls](ai%20examples/01_DrawRoomWithWalls.md), [02. Draw 2D Geometry Primitives](ai%20examples/02_Draw2DPrimitives.md), [03. Build a Curved Path with Mixed Vertex Types](ai%20examples/03_CurvedPolylinePath.md), [04. Extrude 2D Shapes into 3D Solids](ai%20examples/04_ExtrudeShapesTo3D.md)

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
