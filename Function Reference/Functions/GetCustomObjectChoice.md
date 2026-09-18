# GetCustomObjectChoice

## Description
Function GetCustomObjectChoice returns a choice string of the specified plug-in object popup menu or radio group parameter.  These parameters are displayed in the Object Info palette or the plug-in objects' creation dialog.

The string passed into the parameter name argument should use the parameter constant syntax, not the actual parameter name.  The string should have the prefix character 'P', and should have all spaces replaced with underscore characters.  For example, a parameter Jamb Depth would have a constant declared as PJAMB_DEPTH and therefore the parameter name argument to this function should be the string 'PJAMB_DEPTH'. 

The choiceIndex parameter should be passed an integer between 1 and the number of choices, which can be determined by calling the NumCustomObjectChoices function.

```pascal
FUNCTION GetCustomObjectChoice(
				objectName    : STRING;
				parameterName : STRING;
				choiceIndex   : INTEGER): STRING;
```

```python
def vs.GetCustomObjectChoice(objectName, parameterName, choiceIndex):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|Name of the plugin object.|
|parameterName|STRING|String indicating which parameter.|
|choiceIndex|INTEGER|Index of desired choice.|

## Remarks
Call from CustomObject scripts only.  Returns a particular choice string for a popup menu or radio group parameter.

## Examples
#### VectorScript ####
```pascal
theChoice := GetCustomObjectChoice(objectName, 'PDINNER_MENU', 1);
```
#### Python ####
```python
theChoice = vs.GetCustomObjectChoice(objectName, 'PDINNER_MENU', 1)
```

```pascal
BEGIN
	formatH := GetObject (pluginName);
	IF pMethod = GetCustomObjectChoice (pluginName, 'pMethod', 2) THEN method := 2
	ELSE method := 1;

BEGIN
	gSize := GetCustomObjectChoice( gPluginName, fieldName, NumCustomObjectChoices( gPluginName, fieldName ) );
	SetRField( formatHand, gPluginName, fieldName, gSize );
END;

		gBubbleDisplay_idx := 1;
		gNumDisplay_idx := 2;
		END;
	END; {Case}
SetRfield(parmHand,parmName,'fConfig',GetCustomObjectChoice(parmName,'fConfig',gBubbleDisplay_idx));
SetRfield(parmHand,parmName,'Num Config',GetCustomObjectChoice(parmName,'Num Config',gNumDisplay_idx));
```
```python
import vs

# Function GetCustomObjectChoice returns a choice string of the specified
# plug-in object popup menu or radio group parameter.
objectName = 'Example'
parameterName = 'Example'
choiceIndex = 1

text = vs.GetCustomObjectChoice(objectName, parameterName, choiceIndex)
vs.Message('GetCustomObjectChoice returned: ' + str(text))
```

## See Also
VS Functions:
[NumCustomObjectChoices](NumCustomObjectChoices.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
