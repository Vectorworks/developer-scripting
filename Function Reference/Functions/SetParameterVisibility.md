# SetParameterVisibility

## Description
For plug-in objects, this procedure sets whether or not the specified parameter is visible on the Object Info Palette.  This routine is used inside plug-in object regeneration scripts to set their parameter visibility.  This visibility is an object instance property.

```pascal
PROCEDURE SetParameterVisibility(
				inPlugin        : HANDLE;
				inParameterName : STRING;
				inSetVisible    : BOOLEAN);
```

```python
def vs.SetParameterVisibility(inPlugin, inParameterName, inSetVisible):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inPlugin|HANDLE|Handle to the currently executing plug-in object.|
|inParameterName|STRING|Name of parameter, as it appears in the plug-in editor's parameter list.|
|inSetVisible|BOOLEAN|The new visibility state for the parameter specified.|

## Remarks
Uses the "ParamName" (not "pParamName").

If you hide a parameter it appears to change the order of the internal list. So, in a multiple selection you may be changing the wrong values and not know it.  i.e.. Objects A and B have the same parameter list.  Hide the first parameter in A using SetParameterVisibility, and the parameters will now align A-B as 1-2,2-3,3-4... in a multiple selection.(26637)

Multiple selections behave differently on Mac and windows.  Select 2 objects.  Object A has a Dim Parm, Object B has an Int Parm.  Change the parm.  On windows, it will change to 11" and 11 respectively.  On the Mac, with A  active it will change to 11" and no change to B.(26635)

## Examples
```pascal
BEGIN
	SetParameterVisibility(parmHand,'LineLength',FALSE);
	PushAttrs;
	Initialize;
	OpenPoly;
	IF (ErrorStatus = FALSE) THEN

BEGIN
IF GetCustomObjectInfo(gParmN,gParmH,gRecH,gWallH) THEN BEGIN
	GetContainerInfo(gParmH,gContainerH,container_tp,LS);
	SetParameterVisibility(gParmH,'LineLength',FALSE);
	GetSymLoc(gParmH,pt1.x,pt1.y);
	IF (container_tp = 11) {I'm in a group}
		THEN temp_b := GetPickObjectInfo(pt1.x,pt1.y,gGroupH,gLine,temp_i)
		ELSE BEGIN

BEGIN
	GetVersion(major, minor, maint, platform);
	SetRField(objHand, objName, '__version', Concat(major, minor, maint));
	SetParameterVisibility(objHand, '__version', FALSE);
END;
```
```python
# Modifiers
useModifiers	= vs.PUse_Site_Modifiers
useFence		= False
vs.SetParameterVisibility( gObjHandle, 'Use Fence', useModifiers )
if useModifiers:
	useFence = vs.PUse_Fence
kStrExistDTM	= vs.GetResourceString( kMiscStrID, 1 )
if ( vs.IsNewCustomObject( gObjName ) ):
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
