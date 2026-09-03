# SetDefaultEndMarker

## Description
Sets all properties of the document default end marker. Return TRUE if operation was successful.

```pascal
FUNCTION SetDefaultEndMarker(
				style          : LONGINT;
				angle          : INTEGER;
				size           : REAL;
				width          : REAL;
				thicknessBasis : INTEGER;
				thickness      : REAL;
				visibility     : BOOLEAN): BOOLEAN;
```

```python
def vs.SetDefaultEndMarker(style, angle, size, width, thicknessBasis, thickness, visibility):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|style|LONGINT|The marker style. (see comments for details)|
|angle|INTEGER|The marker angle in degrees. (0 to 90)|
|size|REAL|The marker size in page inches.|
|width|REAL|The marker width in page inches.|
|thicknessBasis|INTEGER|The marker thickness basis. ( see comments for details)|
|thickness|REAL|The marker thickness.|
|visibility|BOOLEAN|The marker visibility.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
ok : BOOLEAN;
BEGIN
ok := SetDefaultEndMarker(2176, 15, 0.5, 0, 0, 2, TRUE);	
END;

RUN(Example);
```
#### Python ####
```python

```

```pascal
BSB := GetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,viz_beg);
BSB := GetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,viz_end);
{Mark 0,0,0}
BSB := SetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,FALSE);
BSB := SetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,FALSE);
GetVersion(version,vdummy,vdummy,vdummy);
IF (version > 9) THEN SetObjectVariableBoolean(parmHand, kFontPropertySelector, TRUE);
pathHand := GetCustomObjectPath(parmHand);
Path_Area_Handler(parmHand, pathHand, FALSE, TRUE, TRUE, FALSE);

{FMar}
BSB := GetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,viz_beg);
BSB := GetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,viz_end);
BSB := SetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,FALSE);
BSB := SetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,FALSE);
Loop(x, y, x2, y2, kLassoDia);
SetLW ( LNewObj, kThLnWeight);
IF (gTagIdx = 2) THEN j := -1 ELSE j := 1;
IF IsObjectFlipped(hSourceObj) THEN i := -1 ELSE i := 1;

IF pArrows<>kRaStrNone  THEN BEGIN
	pushattrs;
	BSB := GetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,viz_beg);
	BSB := GetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,viz_end);
	BSB := SetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,FALSE);
```
```python
result = vs.SetDefaultEndMarker(style, 1.0, 2.0, 0.5, 1.0, 2.0, True)
```

## See Also
VS Functions:
[SetDefaultBeginningMarker](SetDefaultBeginningMarker.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
