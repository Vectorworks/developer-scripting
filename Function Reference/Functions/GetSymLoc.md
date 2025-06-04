# GetSymLoc

## Description
Procedure GetSymLoc returns the insertion point of the referenced symbol or plug-in object.

```pascal
PROCEDURE GetSymLoc(
				symHd     : HANDLE;
				VAR pX,pY : REAL);
```

```python
def vs.GetSymLoc(symHd):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|symHd|HANDLE|Handle to placed symbol.|
|p|REAL|Returns insertion point of symbol|

## Remarks
You can use this function to retrieve the position of a PlugIn Object, from within the PlugIn Object itself. However, it will only display its position relative to the internal origin. 
Gerard Jonkers, 2007/01/08: See also my [http://www.vectorlab.info/index.php?title=Absolute_Origin Absolute_Origin] article about origins on the VectorLab.

## Examples
Example, code for the PIO:
```pascal
Procedure HereAmI;
VAR
hParm, hParmRecord, hWall : HANDLE;
PIOName, txtStr: STRING;
x, y : REAL;
BEGIN
IF GetCustomObjectInfo(PIOName, hParm, hParmRecord, hWall) THEN
BEGIN
GetSymLoc(hParm, x, y);
txtStr:= Concat(x, ' / ', y);
Locus(0, 0);
TextOrigin(0, 0);
BeginText;
txtStr
EndText;
END;
END;
Run (HereAmI);
```
==== Python ====
```python
def HereAmI():
	hasObj, PIOName, hParm, hParmRecord, hWall = vs.GetCustomObjectInfo()
	if hasObj:
		ptXY = vs.GetSymLoc(hParm)
		txtStr = vs.Concat(ptXY[0], ' / ', ptXY[1])
		vs.Locus(0, 0)
		vs.TextOrigin(0, 0)
		vs.BeginText()
		txtStr
		vs.EndText()
HereAmI()
```

## Version
Availability: from All Versions

## Category
* [Object Info](../Categories/Object%20Info.md)
