# FindObjAtPt_Create

## Description
Creates object find for objects at specified point within specified radius. The function is capable of iterating

```pascal
FUNCTION FindObjAtPt_Create(
				hContainer  : HANDLE;
				objOptions  : INTEGER;
				travOptions : INTEGER;
				locX        : REAL;
				locY        : REAL;
				pickRadius  : REAL): LONGINT;
```

```python
def vs.FindObjAtPt_Create(hContainer, objOptions, travOptions, locX, locY, pickRadius):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hContainer|HANDLE|   |
|objOptions|INTEGER|AllObjs = 0; VisibleOnly = 1; SelectedOnly = 2; UnlockedOnly = 3|
|travOptions|INTEGER|Shallow = 0; Groups = 1|
|locX|REAL|   |
|locY|REAL|   |
|pickRadius|REAL|   |

## Remarks
(*_c_*, 2011): Was undocumented, made public by VW 2012 (1700).

(*_c_*, 2008-10-15): Finds objects at the point "Loc" starting from the parent container "hContainer". The routine returns a longint as list of objects (similar to [BuildResourceList](BuildResourceList.md)) which you'll use to manipulate the found objects. The suffix ''create'' stays then for ''create a list''.
* [FindObjAtPt_GetCount.md](FindObjAtPt_GetCount.md) will return the count of found objects
* [FindObjAtPt_GetObj.md](FindObjAtPt_GetObj.md) returns a handle to the object at index i. The index is 0-based.

It seems to ignore most object types. It will work with: lines, polylines, polygons, rectangles, arcs, 2D loci, pios. Notably it will ignore: walls, symbols, round rects, ovals, 3D polys, 3D loci, nurbs, extrudes, dimensions, slabs, roofs....

rgm, 2016-10-05 : for objOptions it's 0 for AllObjs, 1 for VisibleOnly, 2 for SelectedOnly, 3 for UnlockedOnly; travOptions is 0 for Shallow and 1 for Groups (from `FindObjectAtPoint.h` in the SDK).

<code lang="pas">
PROCEDURE xxxxx;
VAR
	cnt, i : INTEGER;
	startContainer : HANDLE;
	list : LONGINT;
	loc	: VECTOR;
		
BEGIN
	GetPt(loc.x, loc.y);
	startContainer := NIL;
	
	list := FindObjAtPt_Create(startContainer, 1, 0, loc.x, loc.y, 100);
	cnt := FindObjAtPt_GetCount(list);
	
	i := 0;
	WHILE i < cnt DO BEGIN
		AlrtDialog(Concat('Index: ', i, ' Obj Type: ', GetTypeN(FindObjAtPt_GetObj(list, i))));
		i := i + 1;
	END;
	FindObjAtPt_Delete( list );
END;
Run(xxxxx);</code>

<code lang='py'>
def PickPointCallback(pt):
	startContainer = vs.Handle();
	
	list = vs.FindObjAtPt_Create(startContainer, 1, 0, pt[0], pt[1], 100)
	cnt = vs.FindObjAtPt_GetCount(list)
	
	for(i in range(cnt):
		hObj = vs.FindObjAtPt_GetObj( list, i );
		vs.AlrtDialog( 'Index: ' + str(i) + ' Obj Type: ' + str(vs.GetTypeN(hObj)) )

	vs.FindObjAtPt_Delete( list )


vs.GetPt( PickPointCallback )
</code>

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
