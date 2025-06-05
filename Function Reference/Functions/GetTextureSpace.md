# GetTextureSpace

## Description
Function GetTextureSpace returns a handle to the texture space attached to the referenced object(or object part).

```pascal
FUNCTION GetTextureSpace(
				obj    : HANDLE;
				partID : INTEGER): HANDLE;
```

```python
def vs.GetTextureSpace(obj, partID):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|partID|INTEGER|Part ID (pass 1 for non-supporting objects).|

## Remarks
*_c_*, (2018.12.29) Don't use this: it works but on walls will remove the mapping, tested on VW 2017, 2018. The new GetTexMapXXX routines accept a direct object handle, without needing the texture space handle.


Returns the texture space attached to this object, with the same part ID as partID.  Walls may have three texture spaces attached to them if they have expanded textures, for example.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example; 
VAR
XAxis, YAxis, ZAxis :REAL; 
hObj :HANDLE; 
BEGIN
hObj := GetTextureSpace(FSActLayer, 0); 
GetTexSpaceOrientU(hObj, XAxis, YAxis, ZAxis); 
Writeln('U', ' : ', XAxis, ' : ', YAxis, ' : ', ZAxis); 
GetTexSpaceOrientV(hObj, XAxis, YAxis, ZAxis); 
Writeln('V', ' : ', XAxis, ' : ', YAxis, ' : ', ZAxis); 
GetTexSpaceOrientW(hObj, XAxis, YAxis, ZAxis); 
Writeln('W', ' : ', XAxis, ' : ', YAxis, ' : ', ZAxis); 
END; 
RUN(Example);
```
#### Python ####
```python
def Example():
	hObj = vs.GetTextureSpace(vs.FSActLayer(), 0)
	XAxis, YAxis, ZAxis = vs.GetTexSpaceOrientU(hObj)
	vs.Message('U', ' : ', XAxis, ' : ', YAxis, ' : ', ZAxis)
	XAxis, YAxis, ZAxis = vs.GetTexSpaceOrientV(hObj) 
	vs.Message('V', ' : ', XAxis, ' : ', YAxis, ' : ', ZAxis)
	XAxis, YAxis, ZAxis = vs.GetTexSpaceOrientW(hObj)
	vs.Message('W', ' : ', XAxis, ' : ', YAxis, ' : ', ZAxis)

Example()
```

## Version
Availability: from VectorWorks 8.0

## Category
* [Textures](../Categories/Textures.md)
