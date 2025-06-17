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

## See Also
VS Functions:
[GetLocalizedPluginName](GetLocalizedPluginName.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
