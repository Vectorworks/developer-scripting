# DotProduct

## Description
Returns the dot product of the two specified vectors.

The dot product is also known as the scalar product of the two vectors, and is equivalent to the product of the magnitudes of the two vectors multiplied by the cosine of the angle between the two vectors.

```pascal
FUNCTION DotProduct(
				v1 : VECTOR;
				v2 : VECTOR): REAL;
```

```python
def vs.DotProduct(v1, v2):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v1|VECTOR|Source vector 1.|
|v2|VECTOR|Source vector 2.|

## Remarks
([[User:CBM-c-|_c_]], 2022.01.20) In Python the two vectors used as parameters MUST be 3-dimensional, or it will return gibberish. This doesn't matter in Pascal.

<code lang="py">
# EXAMPLE OF FAULTY USAGE
v1 = (12, 1) # bidimensional
v2 = (3, 15) 
vs.Message( str(vs.DotProduct(v1, v2)) ) # returns gibberish
</code>

''' other comments whose author/date is lost:'''

(PCP ): This should be used in place of the bullet/yen operator for better cross-platform operability. -

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
    pt1, pt2, pt3, pt4 :VECTOR;
    ang :REAL;
BEGIN
    GetPt(pt1.x, pt1.y);
    GetPtL(pt1.x, pt1.y, pt2.x, pt2.y);
    GetPtL(pt2.x, pt2.y, pt3.x, pt3.y);

    MoveTo(pt1.x, pt1.y);
    LineTo(pt2.x, pt2.y);
    LineTo(pt3.x, pt3.y);
    pt4 := (pt1 + pt3) / 2;

    { Find the angle between the vectors.}
    ang := Rad2Deg(ArcCos(DotProduct(UnitVec(pt1-pt2), UnitVec(pt3-pt2))));
    TextOrigin(pt4.x, pt4.y);
    CreateText(Concat(ang));
END;
RUN(Example);
```
==== Python ====
```python
v1 = (12, 1, 0) # 3-dimensional tuple
v2 = (3, 15, 0) 
vs.Message( str(vs.DotProduct(v1, v2)) )
```

## See Also
VS Functions:
[AngBVec](AngBVec.md)

## Version
Availability: from VectorWorks 8.0

## Category
* [Math - Vectors](../Categories/Math%20-%20Vectors.md)
