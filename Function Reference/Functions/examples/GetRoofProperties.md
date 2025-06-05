==== VectorScript ====
```pascal
PROCEDURE Example;

PROCEDURE ShowRoofFaceAttrib(roofFace :HANDLE);
VAR
roofRise, roofRun :REAL; 
miterType, holeStyle :INTEGER; 
vertPart, thickness :REAL;
beg_pt, end_pt, upslope_pt :VECTOR;
Z :REAL;
BEGIN
IF GetObjectVariableInt(roofFace, 172) = 1 THEN BEGIN
GetRoofFaceAttrib(roofFace, roofRise, roofRun, miterType, holeStyle, vertPart, thickness);
Message('roofRise: ', roofRise,
',  roofRun: ', roofRun,
',  miterType: ', miterType,
',  holeStyle: ', holeStyle,
',  vertPart: ', vertPart,
',  thickness: ', thickness);

GetRoofFaceCoords(roofFace, beg_pt.x, beg_pt.y, end_pt.x, end_pt.y, Z, upslope_pt.x, upslope_pt.y);
beg_pt     := beg_pt     * (25.4 / GetPrefReal(152));
end_pt     := end_pt     * (25.4 / GetPrefReal(152));
upslope_pt := upslope_pt * (25.4 / GetPrefReal(152));
Locus(beg_pt.x, beg_pt.y);
Locus(end_pt.x, end_pt.y);
Locus(upslope_pt.x, upslope_pt.y);
END;
END;

BEGIN
 ForEachObject(ShowRoofFaceAttrib, ((T=71)));
END;
RUN(Example);
```

==== Python ====
```python
def ShowRoofFaceAttrib(roofFace):
	if vs.GetObjectVariableInt(roofFace, 172) == 1:
		roofRise, roofRun, miterType, holeStyle, vertPart, thickness = vs.GetRoofFaceAttrib(roofFace)
		vs.Message('roofRise: ', roofRise,
		',  roofRun: ', roofRun,
		',  miterType: ', miterType,
		',  holeStyle: ', holeStyle,
		',  vertPart: ', vertPart,
		',  thickness: ', thickness)
		
		beg_pt, end_pt, Z, upslope_pt = vs.GetRoofFaceCoords(roofFace)
		
			
		
		vs.Locus(beg_pt[0]    * (25.4 / vs.GetPrefReal(152)), beg_pt[1]    * (25.4 / vs.GetPrefReal(152)));
		vs.Locus(end_pt[0]    * (25.4 / vs.GetPrefReal(152)), end_pt[1]    * (25.4 / vs.GetPrefReal(152)))
		vs.Locus(upslope_pt[0]    * (25.4 / vs.GetPrefReal(152)), upslope_pt[1]    * (25.4 / vs.GetPrefReal(152)));


def Example():
	vs.ForEachObject(ShowRoofFaceAttrib, '((T=71))')

Example()
```
