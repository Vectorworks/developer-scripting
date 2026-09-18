# GetCustomObjectInfo

## Description
Function GetCustomObjectInfo is used within plug-in object scripts to determine information about the object. Returns TRUE when (objectHand <> NIL) AND (recordHand <> NIL)

```pascal
FUNCTION GetCustomObjectInfo(
				VAR objectName : STRING;
				VAR objectHand : HANDLE;
				VAR recordHand : HANDLE;
				VAR wallHand   : HANDLE): BOOLEAN;
```

```python
def vs.GetCustomObjectInfo():
    return (BOOLEAN, objectName, objectHand, recordHand, wallHand)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|Returns the name of the object.|
|objectHand|HANDLE|Returns a handle to the plugin object in the drawing.|
|recordHand|HANDLE|Returns a handle to the record containing current parameter values.|
|wallHand|HANDLE|Returns a handle to a wall, (if this object is in a wall).|

## Remarks
[sd 8/19/98]

## Examples
```pascal
BEGIN
	bsb := GetCustomObjectInfo(parmName, parmHand, parmRecordHand, wallHand);
	vsoGetEventInfo(theEvent, theButton);
	CASE theEvent OF
		kObjOnInitXProperties:
			BEGIN

BEGIN
{* Main program *}
	result := GetCustomObjectInfo(pluginName, pluginH, recordH, wallH);
	VSOGetEventInfo(eventID,eventMessage);
	CASE eventID OF
		 kObjOnInitXProperties:
			BEGIN

BEGIN
IF GetCustomObjectInfo(gParmN,gParmH,gRecH,gWallH) THEN BEGIN
	GetContainerInfo(gParmH,gContainerH,container_tp,LS);
	SetParameterVisibility(gParmH,'LineLength',FALSE);
	GetSymLoc(gParmH,pt1.x,pt1.y);
	IF (container_tp = 11) {I'm in a group}
		THEN temp_b := GetPickObjectInfo(pt1.x,pt1.y,gGroupH,gLine,temp_i)
```
```python
ok, gObjName, gObjHandle, gRecordHandle, gWallHandle = vs.GetCustomObjectInfo()

def SetUpObject():
	succeeded = False
	saveClass = ''
	ok, objectName, objectHand, recordHand, wallHand = vs.GetCustomObjectInfo()
	if ok and ResourceIsOK():
		vs.PushAttrs()
		vs.Marker( 0, 0, 0 )
		if objectHand != None:

def execute():
	# Define globals
	global gObjName, gObjHandle, gRecordHandle, gWallHandle
	ok, gObjName, gObjHandle, gRecordHandle, gWallHandle = vs.GetCustomObjectInfo()
	if gObjHandle == None:
		gObjName = 'Roadway (Curved)'
		gObjHandle	= vs.GetObject( gObjName )	# get format, it is important for tool events!!
```
See also in tutorials: [Plug-in with widgets, basic example (Python)](../../Common/Tasks/Parametrics/Plug-in%20with%20widget%20basic%20example.md)

## See Also
VS Functions:
[IsNewCustomObject](IsNewCustomObject.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
