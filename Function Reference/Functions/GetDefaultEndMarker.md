# GetDefaultEndMarker

## Description
Gets all properties for the document default end marker. Return TRUE if operation was successful.

```pascal
FUNCTION GetDefaultEndMarker(
				VAR style          : LONGINT;
				VAR angle          : INTEGER;
				VAR size           : REAL;
				VAR width          : REAL;
				VAR thicknessBasis : INTEGER;
				VAR thickness      : REAL;
				VAR visibility     : BOOLEAN): BOOLEAN;
```

```python
def vs.GetDefaultEndMarker():
    return (BOOLEAN, style, angle, size, width, thicknessBasis, thickness, visibility)
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
style: INTEGER;
angle: INTEGER;
size: REAL;
width: REAL;
thickBasis: INTEGER;
thickness: REAL;
visibility: BOOLEAN;

BEGIN
ok := GetDefaultEndMarker (style, angle, size, width, thickBasis, thickness, visibility);
Message (style, ' /  ', angle, '  /  ', size, '  /  ', width, ' /  ', thickBasis, ' /  ', thickness, ' /  ', visibility);	
END;

RUN(Example);
```
#### Python ####
```python
def Example():
	ok, style, angle, size, width, thickBasis, thickness, visibility = vs.GetDefaultEndMarker ()
	vs.Message (style, ' /  ', angle, '  /  ', size, '  /  ', width, ' /  ', thickBasis, ' /  ', thickness, ' /  ', visibility)

Example()
```

```pascal
EnableParameter(parmHand,kLenFldName,FALSE); {Fixes bug B055311 - RFA - 02/02/07}
dimstd := getprefint(71);
{fMark}
BSB := GetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,viz_beg);
BSB := GetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,viz_end);
{Mark 0,0,0}
BSB := SetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,FALSE);
BSB := SetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,FALSE);
GetVersion(version,vdummy,vdummy,vdummy);

BEGIN
arrowindex := str2num(copy(pArrowStyle,1,1));
BSB := GetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,viz_beg);
BSB := GetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,viz_end);
BSB := SetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,FALSE);
CASE arrowindex OF
	0: BSB := SetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,FALSE);{Mrk(0,0.25 * pMkrScaleFactor,15);}
	1: BSB := SetDefaultEndMarker(0,15,0.25 * pMkrScaleFactor,0,2,2,TRUE);{Mrk(2,0.25 * pMkrScaleFactor,15);}

BEGIN
	{FMar}
	BSB := GetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,viz_beg);
	BSB := GetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,viz_end);
	BSB := SetDefaultBeginningMarker(mStyle_beg,ang_beg,leng_beg,wid_beg,tBasis_beg,thk_beg,FALSE);
	BSB := SetDefaultEndMarker(mStyle_end,ang_end,leng_end,wid_end,tBasis_end,thk_end,FALSE);
	Loop(x, y, x2, y2, kLassoDia);
	SetLW ( LNewObj, kThLnWeight);
```
```python
import vs

# Gets all properties for the document default end marker.
ok, style, angle, size, width, thicknessBasis, thickness, visibility = vs.GetDefaultEndMarker()
vs.Message('GetDefaultEndMarker returned: ' + str((ok, style, angle, size, width, thicknessBasis, thickness, visibility)))
```

## See Also
VS Functions:
[GetDefaultBeginningMarker](GetDefaultBeginningMarker.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
