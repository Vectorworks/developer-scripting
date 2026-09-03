# ReleaseXML

## Description
Frees memory associated with the specified XMLHandle. Once this function is called, XMLHandle can no longer be used.

```pascal
FUNCTION ReleaseXML(XMLHandle : LONGINT):INTEGER;
```

```python
def vs.ReleaseXML(XMLHandle):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|XMLHandle|LONGINT|   |

## Examples
[XMLParse](examples/XMLParse.md)

```pascal
	closeShapeStr := GetElement(xmlID, 'PropertyLine/closeShape');
	IF closeShapeStr = ''
		THEN closeShape := TRUE {so it will default to true the first time}
		ELSE closeShape := Str2Boo(GetElement(xmlID, 'PropertyLine/closeShape'));
	xmlID := ReleaseXML(xmlID);
end else BEGIN
	closeShape := GetVertexVisibility(pathHandle, GetVertNum(pathHandle) - 1);
	GetSymLoc(objHand, originPt.x, originPt.y);
	objectRotation := GetSymRot(objHand);

BEGIN
	OpenXML(xmlID);
	gEditReal7   := Str2Num(GetElement(xmlID, 'StairAssembly/gEditReal7'));
	gEditReal8   := Str2Num(GetElement(xmlID, 'StairAssembly/gEditReal8'));
	xmlID := ReleaseXML(xmlID);
	IF ResourceIsOK THEN stairCalc_Setup;
	IF RunNamedDialog(stairCalc, stairCalc_Handler, 'StairPreferences') = 1 then BEGIN
		stairCalc_Main := TRUE;
		OpenXML(xmlID);

useDefCon := GetPref(130);
SetPref(130, TRUE);
OpenXML(xmlID);
symName := GetElement(xmlID, 'StairSymbolDialog/symName');
xmlID := ReleaseXML(xmlID);
dialogTitle		:= GetPlugInString(3010); {Select a Stair Config}
dialogHelpStr	:= 'SelectStairConfiguration_Custom';
if SelectSymbolDialog(dialogTitle, dialogHelpStr,'StairSymbol1', -kDefaultCustomStair, '', '', symName) = 1 then BEGIN
	ChooseStairConfig := 1;
```
```python
import vs

# Frees memory associated with the specified XMLHandle.
XMLHandle = 1

resultN = vs.ReleaseXML(XMLHandle)
vs.Message('ReleaseXML returned: ' + str(resultN))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [XML](../Categories/XML.md)
