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

## See Also
VS Functions:
[AlertInform](AlertInform.md) 
| [AlertCritical](AlertCritical.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
