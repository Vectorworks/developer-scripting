# GetNumHoles

## Description
Returns the number of openings in the referenced polyline.

```pascal
FUNCTION GetNumHoles(
				inPolyline      : HANDLE;
				VAR outNumHoles : INTEGER): BOOLEAN;
```

```python
def vs.GetNumHoles(inPolyline):
    return (BOOLEAN, outNumHoles)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inPolyline|HANDLE|Handle to polyline.|
|outNumHoles|INTEGER|The number of openings in the polyline object.|

## Remarks
This function never returns FALSE regardless of the object type of "inPolyline" or whether "inPolyline" has holes.
It will only return FALSE on "inPolyine" = NIL.

## Examples
```pascal
	GetPolyPt(h1, 1,              pt1.x, pt1.y);
	GetPolyPt(h1, GetVertNum(h1), pt2.x, pt2.y);
	IF Abs(Norm(pt2 - pt1)) < .0625" THEN DelVertex(h1, GetVertNum(h1));
END;
IF doNet & GetNumHoles(walls[cnt1], hole_cnt) THEN BEGIN
	for cnt2 := 1 to hole_cnt do if GetHole(walls[cnt1], cnt2, h2) then BEGIN
		h2 := OffsetPolygon(h2, 1");
		for cnt4 := GetVertNum(h2) downto 2 do BEGIN
			GetPolyPt(h2, cnt4 - 1, pt1.x, pt1.y);
			GetPolyPt(h2, cnt4,     pt2.x, pt2.y);
			IF Abs(Norm(pt2 - pt1)) < .0625" THEN DelVertex(h2, cnt4);

EndPoly;
new_out_poly_h := lnewobj;
{handle holes}
IF (gettype(h) = 21) THEN BEGIN
	temp_b := getnumholes(h,holenum);
	IF (holenum > 0) THEN FOR i := 1 TO holenum DO BEGIN
		temp_b := gethole(h,i,hole_OF_interest);
		temp_b := addhole(new_out_poly_h,hole_OF_interest);
		END;

BEGIN
IF GetNumHoles(pLine_obj,gHoleNum) & (gHoleNum > 0) THEN
	BEGIN
	gHasHoles := TRUE;
	ALLOCATE gHoles[1..gHoleNum];
	FOR i := 1 TO gHoleNum DO result := GetHole(pLine_obj,i,gHoles[i]);
	END ELSE gHasHoles := FALSE;
END;
```
```python
import vs

# Returns the number of openings in the referenced polyline.
inPolyline = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, outNumHoles = vs.GetNumHoles(inPolyline)
vs.Message('GetNumHoles returned: ' + str((ok, outNumHoles)))
```

## See Also
VS Functions:
[GetHole](GetHole.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
