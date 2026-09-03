# GetLocalizedPluginParameter

## Description
Get the localized name of a plug-in parameter.

When VectorWorks plug-ins are localized by distributors in other countries, their parameter names are translated to the appropriate language.  The plug-in file stores both the original universal name and this translated localized name for each parameter.  The translated name is displayed by the VectorWorks user interface instead of the original name.  If a script needs to display the name of a plug-in parameter in a dialog or message then it should call this function to determine the localized name.  (Note that scripts will use the universal name to specify a plug-in parameter when the name is not being displayed to the user.) 

If the plug-in has not been localized, then this function will return the universal name of the parameter.

```pascal
FUNCTION GetLocalizedPluginParameter(
				inPluginName     : STRING;
				inParameterName  : STRING;
				VAR outParameter : STRING): BOOLEAN;
```

```python
def vs.GetLocalizedPluginParameter(inPluginName, inParameterName):
    return (BOOLEAN, outParameter)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inPluginName|STRING|Universal name of the plug-in.|
|inParameterName|STRING|Universal name of the parameter.|
|outParameter|STRING|Localized name of the parameter.|

## Remarks
An example, from Petri:
```pascal
PROCEDURE ParameterList; { (c) Petri Sakkinen 2008 }
{ Writes the names & "localised" names of the selected PIO to a text file. }

VAR
obHd, recHd :HANDLE;
i, fCount :INTEGER;
rName, fName, localName :STRING;
OK :BOOLEAN; 

PROCEDURE WriteFieldNames;
BEGIN
FOR i := 1 TO fCount DO BEGIN
fName := GetFldName(recHd, i);
ok := GetLocalizedPluginParameter(rName, fName, localName);
Write(fName);
Write(Chr(9));
WriteLn(localName);
END;
END;

BEGIN
obHd := FSActLayer;
recHd := GetRecord(obHd, NumRecords(obHd)); { The PIO record is always the last one. }
rName := GetName(recHd);
PutFile('Parameter listing', rName, fName);
IF NOT DidCancel THEN BEGIN
fCount := NumFields(recHd);
ReWrite(fName);
WriteFieldNames;
Close(fName);
END;
END;
RUN(ParameterList);
```

## Examples
```pascal
BEGIN
	str1 := GetLocStr (11000, 21);
	str2 := GetLocStr (11000, 22);
	OK := GetLocalizedPluginParameter (objName, paramName, locParamName);
	IF paramType = 2 THEN
	BEGIN
		SetRField (objHand, objName, paramName, Num2Str (GetPrefLongInt (162), paramValue));
		alertMsg := Concat (locParamName, str1, Num2Str (GetPrefLongInt (162), lowerLimit), str2, Num2Str (GetPrefLongInt (169), upperLimit));

IF GetLocalizedPluginParameter('Data Stamp','Date',wString) THEN
	status := vsoAppendParamWidget( 1, wString, 0 );
IF GetLocalizedPluginParameter('Data Stamp','Time',wString) THEN
	status := vsoAppendParamWidget( 2, wString, 0 );
IF GetLocalizedPluginParameter('Data Stamp','FNam',wString) THEN
	status := vsoAppendParamWidget( 3, wString, 0 );

IF GetLocalizedPluginParameter('Drawing Label','Title',wString) THEN
	bsb := vsoAppendParamWidget( 1, wString, 0 );
IF GetLocalizedPluginParameter('Drawing Label','Title Alignment',wString) THEN
	bsb := vsoAppendParamWidget( 2, wString, 0 );
IF GetLocalizedPluginParameter('Drawing Label','Drawing',wString) THEN
	bsb := vsoAppendParamWidget( 3, wString, 0 );
```
```python
import vs

# Get the localized name of a plug-in parameter.
inPluginName = 'Example'
inParameterName = 'Example'

ok, outParameter = vs.GetLocalizedPluginParameter(inPluginName, inParameterName)
vs.Message('GetLocalizedPluginParameter returned: ' + str((ok, outParameter)))
```
See also in tutorials: [Plug-in with widgets, basic example (Python)](../../Common/Tasks/Parametrics/Plug-in%20with%20widget%20basic%20example.md)

## See Also
VS Functions:
[GetLocalizedPluginName](GetLocalizedPluginName.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
