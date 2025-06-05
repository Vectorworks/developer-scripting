# CreateSurfacefromCurvesNetwork

## Description
This function will create a NURBS surface from a network of selected intersecting curves in the document

```pascal
FUNCTION CreateSurfacefromCurvesNetwork : BOOLEAN;
```

```python
def vs.CreateSurfacefromCurvesNetwork():
    return BOOLEAN
```

## Remarks
([[User:Orso.b.schmid|Orso]], 2011 Jan. 01) The rountine fails:
* upon invalid objects in the active selection. Before creating the curves through [ CreateNurbsCurve](CreateNurbsCurve.md) you need then to deselect all using [ DSelectAll](DSelectAll.md). If used in PIO deselecting only affects the objects created during the PIO code. After creating the needed curve network through repeated calls of [ CreateNurbsCurve](CreateNurbsCurve.md) you can launch ''CreateSurfacefromCurvesNetwork''.
* on open curve networks. Be careful that your network is perfectly closed.
* often (but not always) on curves whose vertexes don't reside on a plane. It is advisable to set all vertex of the curves forming the network to z-values on a common plane, otherwise the surface even if generated is faulty and displays an excessive amount of vertexes (BTW, this happens also using the command ''Create Surface from Curves'' on drawing). A curve network whose z-values reside on a plane will generate the simplest surface, which can be then refined in the z-values as needed.

([[User:Orso.b.schmid|Orso]], 2010 Dec. 29) This is one of those routines that doesn't respond to [ LNewObj](LNewObj.md). You can access the generated surface through [ PrevObj](PrevObj.md) setting a temporary object after the call.
<code lang="pas">
{ draws a triangle as NURBS curve, converts it to NURBS Surface and tests LNewObj on this last obj }
PROCEDURE CreateNurbsSurf;
VAR
	h : HANDLE;
	pStart : VECTOR;
BEGIN
	GetPt(pStart.x, pStart.y); { fetch starting pt from user }

	{ draw edgy NURBS curve }
	h := CreateNurbsCurve(pStart.x -1m, pStart.y, pStart.z, TRUE, 1);
		AddVertex3D(h, pStart.x +1m, pStart.y, pStart.z);
		AddVertex3D(h, pStart.x, pStart.y +1m, pStart.z);
		AddVertex3D(h, pStart.x -1m, pStart.y, pStart.z);
	
	IF CreateSurfacefromCurvesNetwork THEN BEGIN
		IF YNDialog('try getting a handle to the new NURBS surface using "LNewObj"?') THEN
			h := LNewObj { I expect LNewObj to be the Surface }
		ELSE BEGIN	
			Locus(pStart.x, pStart.y); { temporary obj, you might want to delete it }
			h := PrevObj(LNewObj); { this fetches the Surface }
		END;

		AlrtDialog(Concat( 'Handle "h" should be of type 113 (NURBS surface), now check what I get:', chr(13), GetType(h) ))
	END;
END;
Run(CreateNurbsSurf);</code>

## Version
Availability: from VectorWorks 10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
