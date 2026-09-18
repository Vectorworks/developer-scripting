# GetOrigin

## Description
Procedure GetOrigin returns the current origin location relative to the center of the page.

```pascal
PROCEDURE GetOrigin(
				VAR x : REAL;
				VAR y : REAL);
```

```python
def vs.GetOrigin():
    return (x, y)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|x|REAL|Returns X coordinate of origin.|
|y|REAL|Returns Y coordinate of origin.|

## Remarks
*\_c\_*, 2015.05.31: 
This routine behaves differently across years and usage method:
* until VW 2009:
** used in Commands: returned the User origin shift in current units
** used in Objects: returned {0, 0}
* from VW 2010:
** used in Commands: returns the User origin shift in current units
** used in Objects:  returns the User origin shift in millimeters
Below an example of reading the user origin shift from within a plug-in object. Save the code below as point Plug-in with Reset On Move and Rotation:
```pascal
PROCEDURE HereAmI;
VAR
	pioHandle, pioRecHandle, wallHandle : HANDLE;
	pioName : STRING;
	o, s : VECTOR;

BEGIN
     IF GetCustomObjectInfo(pioName, pioHandle, pioRecHandle, wallHandle) THEN BEGIN
          GetOrigin(o.x, o.y); { on VW 2009 and before this will always be zero when used from within a plug-in object. }
          GetSymLoc(pioH, s.x, s.y);
          Locus(0, 0);
          CreateText(Concat(
               'GetOrigin: ', o, Chr(13), 
               'GetSymLoc: ', s	
          ));
     END;
END;
Run (HereAmI);
```

Objects inside Symbols use the reverse of the User Origin. I added a table of the values related to VectorScript origin in the article [http://www.vectorlab.info/index.php?title=Absolute_Origin#Available_routines:Link Absolute Origin], by Gerard Jonker, on VectorLab.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
originPt : VECTOR;
BEGIN
GetOrigin(originPt.x, originPt.y);
Message(originPt);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	originPtX, originPtY = vs.GetOrigin()
	vs.Message(originPtX, originPtY);
Example()
```

```pascal
angle := GetPrefReal(93);
planrotation := GetPref(92);
SetPref(92, FALSE);
PushAttrs;
GetOrigin(PX, PY);
TextJust (1);
TextVerticalAlign (1);
TextSize (kTextSize);
boxSize := kBoxSize * getUPI * GetLScale (ActLayer);

Options[3] := ''; {Check Box String}
AlertInformDontShowAgain(GetPlugInString(3010),'', FALSE, Options);
PenFore(45000, 45000, 45000);
SetPref(9871, TRUE);
GetOrigin(OriginX,OriginY);
Is3dView := GetProjection(ActLayer)<>6;
RunTempTool(TempToolCallback, TRUE);

BEGIN
	{If origin is not at 0.0 we have to add it to the point in order to get correct object coords}
	GetOrigin(originX, originY);
	pt.x := pt.x + originX;
	pt.y := pt.y + originY;
	pt := WorldToObjectCoords(ObjHand,pt);
	SetRfield(ObjHand,ObjName,'ControlPoint03X',Concat(pt.x));
```
```python
import vs

# Procedure GetOrigin returns the current origin location relative to the
# center of the page.
x, y = vs.GetOrigin()
vs.Message('GetOrigin returned: ' + str((x, y)))
```

## Version
Availability: from All Versions

## Category
* [Document Settings](../Categories/Document%20Settings.md)
