# CreateCustomObjectPath

## Description
Creates an instance of the path custom object specified by the name argument.  The vertices of the path are translated in such a way that the first vertex will be placed at the origin of the plug-in's coordinate space.

```pascal
FUNCTION CreateCustomObjectPath(
				objectName   : STRING;
				path         : HANDLE;
				profileGroup : HANDLE): HANDLE;
```

```python
def vs.CreateCustomObjectPath(objectName, path, profileGroup):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|Name of object.|
|path|HANDLE|Handle to new object path polygon.|
|profileGroup|HANDLE|Handle to new profile group object.|

## Remarks
Calls DefineCustomObject() first to either find the defining FormatNode or create it.  If it is created, the user will be presented with an initialization dialog.  Returns handle to Object.

If the path object code creates a symbol (BeginSym~EndSym), the page center gets messed up, and the only way to fix it is to manually enter and then exit a group or sym def, or to use the previous view button and then the fit to page button. This has been entered as a bug -- I'll remove this comment when the bug is fixed.

It is nothing new, but this routine will create a custom object instance that doesn't resolve as "New Object". If inside the Plug-in code you are using IsNewCustomObject(pioName) you'd expect the object just created to be recognized as new. But IsNewCustomObject will never return TRUE on objects created by CreateCustomObjectPath.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
h :HANDLE;
BEGIN
CallTool(-204);
h := CreateCustomObjectPath('Cutting Plane', FSActLayer, nil);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	vs.CallTool(-204)
	vs.CreateCustomObjectPath('Cutting Plane', vs.FSActLayer(), None)
Example()
```

```pascal
IF objName = 'Property Line Tool' then BEGIN
	if vertCnt > 3 then BEGIN
		DSelectAll;
		HCenter(tmpPath, pt.x, pt.y);
		h := CreateCustomObjectPath('Property Line', tmpPath, NIL);
		pt := WorldToObjectCoords(h, pt);
		SetRField(h, 'Property Line', 'ControlPoint01X', Num2Str(8, pt.x));
		SetRField(h, 'Property Line', 'ControlPoint01Y', Num2Str(8, pt.y));
		SetRField(h, 'Property Line', 'Angle Format',    gAngleFormat);

	addpoint(size_r,0");
	EndPoly;
path_temp_h := lnewobj;
BeginSym(symname_s);
	pio_temp_h := CreateCustomObjectPath('Stipple',path_temp_h,NIL);
	EndSym;
transferdata(PIO2Duplicate,pio_temp_h);
transferattr(PIO2Duplicate,pio_temp_h);
symdef_h := getobject(symname_s);

IF pDrawInside THEN flip := -1 ELSE flip := 1;
IF pDraw3D THEN BEGIN
	EAPprofH := CopyPoly(gShapeH,IsPolyClosed(gShapeH),flip,1,1,gOffX,gOffY);
	EAPpathH := Poly2NURBS(gPathH);
	EAPObjH := createcustomobjectpath('Extrude Along Path',EAPpathH,EAPprofH);
	{Transfer color from continious Profile Object to EAP object}
	{Changing color via the attributes pal will change the color of both profile objects}
	GetFillBack(EAPprofH,R,G,B);
	SetFillBack(EAPObjH,R,G,B);
```
```python
import vs

# Creates an instance of the path custom object specified by the name argument.
objectName = 'Example'
path = 'C:/Temp'
profileGroup = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.CreateCustomObjectPath(objectName, path, profileGroup)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
