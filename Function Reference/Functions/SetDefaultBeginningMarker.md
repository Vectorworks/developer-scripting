# SetDefaultBeginningMarker

## Description
Sets all properties of the document default beginning marker. Return TRUE if operation was successful.

```pascal
FUNCTION SetDefaultBeginningMarker(
				style          : LONGINT;
				angle          : INTEGER;
				size           : REAL;
				width          : REAL;
				thicknessBasis : INTEGER;
				thickness      : REAL;
				visibility     : BOOLEAN): BOOLEAN;
```

```python
def vs.SetDefaultBeginningMarker(style, angle, size, width, thicknessBasis, thickness, visibility):
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
ok := SetDefaultBeginningMarker(2176, 15, 0.5, 0, 0, 2, TRUE);
END;

RUN(Example);
```
#### Python ####
```python

```

```pascal
{fMark}
BSB := GetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,viz_beg);
BSB := GetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,viz_end);
{Mark 0,0,0}
BSB := SetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,FALSE);
BSB := SetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,FALSE);
GetVersion(version,vdummy,vdummy,vdummy);
IF (version > 9) THEN SetObjectVariableBoolean(parmHand, kFontPropertySelector, TRUE);
pathHand := GetCustomObjectPath(parmHand);

BEGIN
arrowindex := str2num(copy(pArrowStyle,1,1));
BSB := GetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,viz_beg);
BSB := GetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,viz_end);
BSB := SetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,FALSE);
CASE arrowindex OF
	0: BSB := SetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,FALSE);{Mrk(0,0.25 * pMkrScaleFactor,15);}
	1: BSB := SetDefaultEndMarker(0,15,0.25 * pMkrScaleFactor,0,2,2,TRUE);{Mrk(2,0.25 * pMkrScaleFactor,15);}
	2: BSB := SetDefaultEndMarker(0,35,0.25 * pMkrScaleFactor,0,2,2,TRUE); {Mrk(2,0.25 * pMkrScaleFactor,35);}

BEGIN
	{FMar}
	BSB := GetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,viz_beg);
	BSB := GetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,viz_end);
	BSB := SetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,FALSE);
	BSB := SetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,FALSE);
	Loop(x, y, x2, y2, kLassoDia);
	SetLW ( LNewObj, kThLnWeight);
	IF (gTagIdx = 2) THEN j := -1 ELSE j := 1;
```
```python
result = vs.SetDefaultBeginningMarker(style, 1.0, 2.0, 0.5, 1.0, 2.0, True)
```

## See Also
VS Functions:
[SetDefaultEndMarker](SetDefaultEndMarker.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
