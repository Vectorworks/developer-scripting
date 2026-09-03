# GetResourceString

## Description
_Deprecated since Vectorworks 2015_: Use [GetVWRString](GetVWRString.md) instead.

<br>
Returns the specified resource string from a resource file.

```pascal
PROCEDURE GetResourceString(
				VAR theString : STRING;
				id            : INTEGER;
				index         : INTEGER);
```

```python
def vs.GetResourceString(id, index):
    return theString
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theString|STRING|The string contained within the resource.|
|id|INTEGER|The ID of the resource.|
|index|INTEGER|The index of the string resource.|

## Examples
```pascal
BEGIN
	GetResourceString( gLocTrue, 2103, 6 );
	GetResourceString( glocFalse, 2103, 7 );
	UprString( gLocTrue  );
	UprString( gLocFalse );
END;

IF ( xmlVersionError_1 <> '' )
	THEN AlrtDialog( Concat( 'xmlVersionError_1: ', xmlVersionError_1 ) )
	ELSE SysBeep;
}
GetResourceString( locTrue, 2103, 6 );
GetResourceString( locFalse, 2103, 7 );
{
AlrtDialog( concat( 'locTrue: ', locTRUE ) );
AlrtDialog( concat( 'locFalse: ', locFALSE ) );

BEGIN
	GetResourceString(D_GetStr, resID, resNr);
END;
```
```python
if objType == 94:
	vs.NameClass( className )
else:
	objectTypeStr = vs.GetResourceString( 11004, objType )
	if objectTypeStr == '':
		objectTypeStr = str(objType)
	msg	= vs.GetResourceString( 11000, 10 ) + className + vs.GetResourceString( 11000, 11 ) + vs.GetResourceString( 11004, objType ) + vs.GetResourceString( 11000, 16 )
	vs.Message( msg )

#  Initialize GetLocStr variables
kStrExistDTM = vs.GetResourceString( kMisc_str_ID, 1 )
vs.ClosePoly()
showPad = vs.PShow_Fences

if useModifiers:
	useFence = vs.PUse_Fence
kStrExistDTM	= vs.GetResourceString( kMiscStrID, 1 )
if ( vs.IsNewCustomObject( gObjName ) ):
	if ( vs.GetObject( kStrExistDTM ) != 0 ):
		vs.SetRField( gObjHandle, gObjName, 'Use Site Modifiers', 'True' )
		useModifiers = True
```

## See Also
VS Functions:
[GetVWRString](GetVWRString.md) , 
[SetVSResourceFile](SetVSResourceFile.md)

## Version
Availability: from VectorWorks 9.0
_Deprecated since Vectorworks 2015_: Use [GetVWRString](GetVWRString.md) instead.

## Category
* [Strings](../Categories/Strings.md)
