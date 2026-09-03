# SetVSResourceFile

## Description
_This function does not do anything in Vectorworks 2015 and later._ This is because the resource system changed. See more at: [[Vectorworks VWR Resources]]

As of Vectorworks 2015, resources are accessed directly by specifying full resource path (resource identifier) and using [GetVWRString](GetVWRString.md)

Pre Vectorworks 2015:
Sets the active resource file for a script. The resource file is opened for the duration of script execution.

The name of the resource file should be specified without the file extension.

```pascal
FUNCTION SetVSResourceFile(fileName : STRING): BOOLEAN;
```

```python
def vs.SetVSResourceFile(fileName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|STRING|The name of the resource file to be opened.|

## Remarks
Specify the file name without an extension. However, the file must exist in the plug-ins folder WITH an extension. Use .rsr on Windows and .rsrc on the Mac.

## Examples
```pascal
If SetVSResourceFile('IP Resources') THEN BEGIN END;

IF SetVSResourceFile('IP Resources') THEN BEGIN END;

gFlag := GetCustomObjectInfo(gPIOName, ghParm, ghParmRecord, ghWall);
gNew := IsNewCustomObject(kPIOName);
vsoGetEventInfo(gTheEvent, gMsgData);
IF SetVSResourceFile('IP Resources') THEN BEGIN END;
```
```python
def ResourceIsOK():
	isOK = False
	if vs.SetVSResourceFile( 'IP Resources' ):
		isOK = True
	else:
		Message( 'The "IP Resources" file was not found.' )
```

## See Also
VS Functions:
[GetResourceString](GetResourceString.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
