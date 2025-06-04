# IntersectSurface

## Description
Creates new surface objects that are the intersection of  the two referenced surface objects. The original surface objects are not modified. The new objects get &quot;inserted&quot; into the drawing list, after s2, and before the next object after that.

```pascal
FUNCTION IntersectSurface(
				s1 : HANDLE;
				s2 : HANDLE): HANDLE;
```

```python
def vs.IntersectSurface(s1, s2):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|s1|HANDLE|Handle to object.|
|s2|HANDLE|Handle to object.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
h1, h2, h3, h4 :HANDLE;
pt :VECTOR;
BEGIN
h1 := NIL;
WHILE h1 = NIL DO BEGIN
Message('Pick the first object...');
GetPt(pt.x, pt.y);
h1 := PickObject(pt.x, pt.y);
END;
h2 := NIL;
WHILE h2 = NIL DO BEGIN
Message('Pick the second object...');
GetPt(pt.x, pt.y);
h2 := PickObject(pt.x, pt.y);
END; 

{Capture the handle of the next object.}
h3 := NextObj(h2);

{Now create the intersection surface(s).}
h4 := IntersectSurface(h1, h2);

{Now find the intersection surface(s).}
WHILE h4 &lt;&gt; h3 DO BEGIN
SetFPat(h4, 3);
h4 := NextObj(h4);
END;
ClrMessage;
END;
RUN(Example);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
