# GetPluginString

## Description
Returns the string specified by stringIndex. The strings are created using the &quot;Strings&quot; button in the plug-in editor.

```pascal
FUNCTION GetPluginString(stringIndex : INTEGER): STRING;
```

```python
def vs.GetPluginString(stringIndex):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|stringIndex|INTEGER|The index of the string as represented in the plug-in editor.|

## Examples
```pascal
BEGIN
	getData := FALSE;
	createErrorMessage2 (GetPlugInString(3001), x0, y0);
END;

theLabel := Concat(GetPlugInString(3004), Chr(13), Chr(13),
					GetPlugInString(3006), Num2Str(2, theta), Chr(13),
					GetPlugInString(3007), Num2StrF(D), Chr(13),
					GetPlugInString(3008), Num2StrF(T), Chr(13),
					GetPlugInString(3009), Num2StrF(L), Chr(13),
					GetPlugInString(3010), Num2StrF(theRadius));

BEGIN
	fieldS [1] := GetPlugInString (3001);
	fieldS [2] := GetPlugInString (3002);
	fieldS [3] := GetPlugInString (3003);
	fieldS [4] := GetPlugInString (3004);
	fieldS [5] := GetPlugInString (3005);
```
```python
def InitParameters():
	# add the widgets
	vs.vsoAddParamWidget( kWidgetID_MarkerSize, 	'Marker Size', '' )
	vs.vsoAppendWidget	( vs.kWidgetButton, 		kWidgetID_StyleButton, vs.GetPluginString( 3002 ), 0 )
	vs.vsoAppendWidget	( vs.kWidgetSeparator, 		kWidgetID_DrawingNumber, vs.GetPluginString( 3003 ), 0 )

from Common.Includes import Utilities_Setup
if ( vs.GetPluginString( 3003 ) != '' ):
	Utilities_Setup.AutoClass( gObjHandle, vs.GetPluginString( 3003 ) )

from Common.Includes import Utilities_Setup
if ( vs.GetPluginString( 3001 ) != '' ):
	Utilities_Setup.AutoClass( gObjHandle, vs.GetPluginString( 3001 ) )
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
