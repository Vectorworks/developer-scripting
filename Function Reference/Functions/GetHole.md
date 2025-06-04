# GetHole

## Description
Returns a handle to a polyline defining an opening within the referenced polyline.

This polyline can be edited or queried using the standard VectorScript polyline API functions.

Hole indexing begins with 1, as with vertex indexing.

```pascal
FUNCTION GetHole(
				inOutsidePolyline : HANDLE;
				inIndex           : INTEGER;
				VAR outHole       : HANDLE): BOOLEAN;
```

```python
def vs.GetHole(inOutsidePolyline, inIndex):
    return (BOOLEAN, outHole)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inOutsidePolyline|HANDLE|Handle to polyline.|
|inIndex|INTEGER|Index number of opening definition polyline.|
|outHole|HANDLE|Handle to definition polyline.|

## Remarks
It is quite fascinating to observe that the parent of a hole has object type "0". Polyline holes reside in Nirvana, so to say....
One would expect their parent to be the polyline container.

<code lang="pas">
PROCEDURE xxxxx;
VAR
temp_i	: INTEGER;
temp_h	: HANDLE;
prefBoo : BOOLEAN;

BEGIN
prefBoo := GetPref(21); { store preference "Stop Vectorscript on warning" }

{ FSActLayer should be a polyline with holes }
IF GetNumHoles(FSActlayer, temp_i) THEN BEGIN
AlrtDialog(concat('HOLES: ', temp_i));

IF GetHole(FSActlayer, temp_i, temp_h) THEN BEGIN
SetPref(21, TRUE); { activate "Stop Vectorscript on warning" }

AlrtDialog(concat('TYPE: ', getType(temp_h)));
AlrtDialog(concat(''TYPE OF PARENT: ', getType(GetParent(temp_h))));
{ this raises a "Handle is NIL" warning }
END ELSE
SysBeep;

SetPref(21, prefBoo); { restore user's "Stop Vectorscript on warning" }
END;
END;

Run(xxxxx);
</code>

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
inPolyline  :HANDLE;
outNumHoles :INTEGER;
inIndex     :INTEGER;
outHole     :HANDLE;
vertexNum   :INTEGER;
pX, pY      :REAL;
vertexType  :INTEGER;
arcRadius   :REAL;
BEGIN
inPolyline := FSActLayer;
IF GetNumHoles(inPolyline, outNumHoles) THEN BEGIN
FOR inIndex := 1 TO outNumHoles DO BEGIN
if GetHole(inPolyline, inIndex, outHole) THEN BEGIN
FOR vertexNum := 1 TO GetVertNum(outHole) DO BEGIN
GetPolylineVertex(outHole, vertexNum, pX, pY, vertexType, arcRadius);
WriteLn('pX: ', pX, ' pY: ', pY);
END;
END;
END;
END;
END;
RUN(Example);
```
==== Python ====
```python
#Labels each vertex of a selected polyline's holes with their hole index and vertex index
def labelHoleVertices():
    inPolyline = vs.FSActLayer()
    hasHole, outNumHoles = vs.GetNumHoles(inPolyline)
    if hasHole:
        for inIndex in range(1,outNumHoles+1):
            hasOutHole, outHole = vs.GetHole(inPolyline, inIndex)
            if hasOutHole:
                for vertexNum in range(1, vs.GetVertNum(outHole)+1):
                    pnt, vertexType, arcRadius = vs.GetPolylineVertex(outHole, vertexNum)
                    vs.MoveTo(pnt)
                    vs.CreateText(str(inIndex) + "." + str(vertexNum))

labelHoleVertices()
```

## See Also
VS Functions:
[GetNumHoles](GetNumHoles.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
