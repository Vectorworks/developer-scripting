# EndXtrd

## Description
Procedure EndXtrd completes the definition of an extrude object within a VectorWorks document. On calling EndXtrd, the object is created in the document from the preceding object creation calls.

It is recommended to call ResetOrientation3D after 3D object creations in order to ensure that the new 3D objects will draw properly.

```pascal
PROCEDURE EndXtrd;
```

```python
def vs.EndXtrd():
    return None
```

## Examples
[BeginXtrd](examples/BeginXtrd.md)

```pascal
BeginXtrd(0',4');
Rect(-1 61/64&quot;,125/128&quot;,-1 119/256&quot;,-375/512&quot;);
Rect(-1 113/512&quot;,1 113/512&quot;,-375/512&quot;,-125/256&quot;);
Rect(-125/256&quot;,125/128&quot;,0',-375/512&quot;);
Rect(125/128&quot;,125/128&quot;,1 119/256&quot;,-375/512&quot;);
Rect(1 25/512&quot;,1 113/512&quot;,375/512&quot;,-125/256&quot;);
Rect(1 363/512&quot;,1 113/512&quot;,2 101/512&quot;,-125/256&quot;);
EndXtrd;
```
#### Python ####
```python

```

```pascal
EndXtrd;
```
```python
# Draw 3D gutter
vs.BeginXtrd( 0, thickness )
DrawGutter( r1, sweep2D, w, gutter, currPenSize)
vs.EndXtrd()
SetAttrsByClassOrParent( vs.LNewObj(), gObjHandle, gPaving_Class )
```
See also in tutorials: [04. Extrude 2D Shapes into 3D Solids](ai%20examples/04_ExtrudeShapesTo3D.md), [06. Boolean Solids: Drill a Hole Through a Block](ai%20examples/06_BooleanSolids.md)

## Version
Availability: from All Versions

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
