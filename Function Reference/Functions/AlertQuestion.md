# AlertQuestion

## Description
Displays an alert dialog which alerts the user to a condition or situation that requires the user's decision and input before preceding; such as an impending action with potentially destructive or irreversible consequences. The message can be in the form of a question.

```pascal
FUNCTION AlertQuestion(
				question           : STRING;
				advice             : STRING;
				defaultButton      : INTEGER;
				OKOverrideText     : STRING;
				CancelOverrideText : STRING;
				customButtonAText  : STRING;
				customButtonBText  : STRING): INTEGER;
```

```python
def vs.AlertQuestion(question, advice, defaultButton, OKOverrideText, CancelOverrideText, customButtonAText, customButtonBText):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|question|STRING|The question to display|
|advice|STRING|The text to be added in a smaller font under the main information/message|
|defaultButton|INTEGER|Specifies which button is to be made the default|0:	the negative(Cancel) button is the default|1:	the positive(Ok) button is the default|2:	custom button A is the default|3:	custom button B is the default|
|OKOverrideText|STRING|Specifies a string to use in overriding the 'OK' string|
|CancelOverrideText|STRING|Specifies a string to use in overriding the 'Cancel' string|
|customButtonAText|STRING|Specifies a string to use for an optional custom button A|
|customButtonBText|STRING|Specifies a string to use for a second optional custom button B|

## Remarks
Examples of all of the messaging techniques:
```AlertQuestion``` uses the exclamation icon, when really it should use the question icon.

## Examples
[AlertDialogsAndMessages](examples/AlertDialogsAndMessages.md)

```pascal
LightFound := FALSE;
CheckedOut := 1;
ForEachObjectInLayer(CheckForLightsOn,0,3,2);
IF LightFound THEN
	CheckedOut := AlertQuestion(GetPluginString(3014),GetPluginString(3017),1,'','','','');

ELSE BEGIN
	alertMsg := Concat (GetPluginString (8019), GetLocStr (12017, 1), GetPluginString (8020), GetLocStr (12017, 4), GetPluginString (8021));
	alertMsg := Concat (alertMsg, GetPluginString (8024), GetLocStr (12017, 4), '.', Chr (13), Chr (13), GetPluginString (8023));
	{* default answer should be yes, so call AlertQuestion directly rather than using wrapper (wrapper defaults to No) ML 5/2014*}
	goAhead := AlertQuestion( alertMsg, '', 1, GetPluginString (8017), GetPluginString (8018), '', '');
END;

	  dialog wouldn't come up and user was stuck. In release it defaulted to eNegative (0). Changed this call
	  to pass in the 0 so the behavior will be the same as before without the assert. But it may not make
	  sense to use a single default for all question dialogs - that's an issue for another time. ML 5/2014
	*}
	AlertDialog := AlertQuestion( theMessage, '', 0, OKString, CancelString, '', '');
END;	{of AlertDialog}
```
```python
import vs

# Displays an alert dialog which alerts the user to a condition or situation
# that requires the user's decision and input before preceding; such as an
# impending.
question = 'Example'
advice = 'Example'
defaultButton = 1
OKOverrideText = 'Example text'
CancelOverrideText = 'Example text'
customButtonAText = 'Example text'
customButtonBText = 'Example text'

resultN = vs.AlertQuestion(question, advice, defaultButton, OKOverrideText, CancelOverrideText, customButtonAText, customButtonBText)
vs.Message('AlertQuestion returned: ' + str(resultN))
```

## See Also
VS Functions:
[AlertInform](AlertInform.md) 
| [AlertCritical](AlertCritical.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
