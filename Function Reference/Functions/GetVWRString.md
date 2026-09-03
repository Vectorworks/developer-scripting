# GetVWRString

## Description
Replaces GetResourceString -- load a string from VWR file
More information about VWR files can be found here [[Vectorworks VWR Resources]].

```pascal
PROCEDURE GetVWRString(
				VAR outputString : STRING;
				resIdentifier    : STRING;
				stringIdentifier : STRING);
```

```python
def vs.GetVWRString(resIdentifier, stringIdentifier):
    return outputString
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outputString|STRING|result value|
|resIdentifier|STRING|VWR identifier and path to vwstrings file|
|stringIdentifier|STRING|key in vwstrings file|

## Remarks
*\_c\_* (2016.08.23): 
GetVWRString is supported by VW 2014, but due to a bug not timely reported, you can’t use it in a subroutine to return the string value. Only directly. This is my workaround (from VW 17/2012):

```pascal
{ _c_ ************************************************ }
{ fix for GetVWRString failing on VW 2014: strings don't set! }
FUNCTION D_GetVWRStr(resID, resNr: INTEGER): STRING;
BEGIN
	GetResourceString(D_GetVWRStr, resID, resNr); 
	{ this silently fails on later versions }
		
	{$IF ver > 19}
	GetVWRString(D_GetVWRStr, Concat(resID), Concat(resNr));
	{$ENDIF}
END;
```

## Examples
```python
vwr = 'EnergyAnalysis/Strings/FormatDef_ThermalBridge.vwstrings'
formatName = vs.GetVWRString(vwr, 'FormatName' )
vs.AlrtDialog( formatName )
```

```pascal
	END;
	IF (str = '') THEN GetVWRString(str,Concat('IP Resources/Strings/',listID,' *'),Concat(stringID));
	GetLocStr := str;
END;

BEGIN
	GetVWRString(angleMark, 'Vectorworks/Strings/1010 Dimension Strings.vwstrings', '10');
	SetRField(parmHand, parmName, 'Selected Heliodon', Concat(city[i], GetPluginString(3008), Num2Str(2, rotation[i]), angleMark));
END;

BEGIN
	If GetLocalizedPluginParameter(recName, fldName, locFldName) then BEGIN
		IF xcoord THEN	GetVWRString(suffix,'Vectorworks/Strings/1150 *','11') {(suffix, 1150, 11 )}
		ELSE			GetVWRString(suffix,'Vectorworks/Strings/1150 *','12');{( suffix, 1150, 12 )}
```
```python
import vs

# Replaces GetResourceString -- load a string from VWR file More information
# about VWR files can be found here [[Vectorworks VWR Resources]].
resIdentifier = 'Example'
stringIdentifier = 'Example'

text = vs.GetVWRString(resIdentifier, stringIdentifier)
vs.Message('GetVWRString returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Strings](../Categories/Strings.md)
