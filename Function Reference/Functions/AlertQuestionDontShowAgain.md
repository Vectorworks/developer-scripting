# AlertQuestionDontShowAgain

## Description
Displays an alert dialog which alerts the user to a condition or situation that requires the user's decision and input before preceding; such as an impending action with potentially destructive or irreversible consequences with the option to always do the selected action and not show the dialog again. The message should be in the form of a question.<BR>
<BR>
The parameter 'arrOptions' is of type ARRAY [1..3] OF STRING;<BR>
arrOpt[1] - Saved setting category to save checkbox value<BR>
arrOpt[2] - Saved setting item to save checkbox value <BR>
arrOpt[3] - Specify a string to use in overriding the default 'Always do the selection action' checkbox string

```pascal
FUNCTION AlertQuestionDontShowAgain(
				question           : STRING;
				advice             : STRING;
				defaultButton      : INTEGER;
				OKOverrideText     : STRING;
				CancelOverrideText : STRING;
				customButtonAText  : STRING;
				customButtonBText  : STRING;
				arrOptions         : ARRAY): INTEGER;
```

```python
def vs.AlertQuestionDontShowAgain(question, advice, defaultButton, OKOverrideText, CancelOverrideText, customButtonAText, customButtonBText, arrOptions):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|question|STRING|The question to display|
|advice|STRING|The text to be added in a smaller font under the main information/message|
|defaultButton|INTEGER|Specifies which button is to be made the default<BR>|0:	the negative button is the default<BR>|1:	the positive button is the default<BR>|2:	custom button A is the default <BR>|3:	custom button B is the default|
|OKOverrideText|STRING|Specifies a string to use in overriding the 'OK' string|
|CancelOverrideText|STRING|Specifies a string to use in overriding the 'Cancel' string|
|customButtonAText|STRING|Specifies a string to use for an optional custom button A|
|customButtonBText|STRING|Specifies a string to use for a second optional custom button B|
|arrOptions|ARRAY|ARRAY [1..3] OF STRING;|arrOpt[1] - Saved setting category to save checkbox value|arrOpt[2] - Saved setting item to save checkbox value|arrOpt[3] - Specify a string to use in overriding the default 'Always do the selection action' checkbox string|

## Remarks
Created by TTF 1/9/2009

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
	result :INTEGER;
	arrayText : ARRAY[1..3] OF STRING;

BEGIN
	arrayText[1] := 'DontShowDialogAgainCategory';
	arrayText[2] := 'DontShowDialogAgainItem'; {Should be unique for every AlertQuestionDontShowAgain}
	arrayText[3] := '';

	result := AlertQuestionDontShowAgain('Do you want to continue?', '', 0, 'Yes', 'No', '', '', arrayText);
END;
RUN(Example);
```
==== Python ====
```python
def Example():
	arrayText = (   'DontShowDialogAgainCategory',
			'DontShowDialogAgainItem', #{Should be unique for every AlertQuestionDontShowAgain}
			'')

        # python uses a tuple
	vs.AlertQuestionDontShowAgain('Do you want to continue?', '', 0, 'Yes', 'No', '', '', arrayText);
Example()
```

## See Also
VS Functions:
[AlertInform](AlertInform.md) 
| [AlertQuestion](AlertQuestion.md) 
| [AlertCritical](AlertCritical.md) 
| [AlertInformDontShowAgain](AlertInformDontShowAgain.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
