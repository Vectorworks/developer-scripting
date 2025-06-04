# AlertInformDontShowAgain

## Description
Displays an alert dialog which provides the user an information about the result of a command with an option to not show the dialog again.  It offers no user choices.<BR>
<BR>
The parameter 'arrOptions' is of type ARRAY [1..3] OF STRING;<BR>
arrOpt[1] - Saved setting category to save checkbox value<BR>
arrOpt[2] - Saved setting item to save checkbox value <BR>
arrOpt[3] - Specify the string to use in overriding the default 'Dont show this dialog again' checkbox string

```pascal
PROCEDURE AlertInformDontShowAgain(
				text       : STRING;
				advice     : STRING;
				minorAlert : BOOLEAN;
				arrOptions : ARRAY);
```

```python
def vs.AlertInformDontShowAgain(text, advice, minorAlert, arrOptions):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|text|STRING|The information to be displayed.|
|advice|STRING|The text to be added in a smaller font under the main information message.|
|minorAlert|BOOLEAN|The severity of the alert: minor(true) or major(false).|
|arrOptions|ARRAY|ARRAY [1..3] OF STRING;|arrOpt[1] - Saved setting category to save checkbox value|arrOpt[2] - Saved setting item to save checkbox value|arrOpt[3] - Specify a string to use in overriding the default 'Dont show this dialog again' checkbox string|

## Remarks
Created by TTF 1/9/2009

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
	result :INTEGER;
	arrayText : ARRAY[1..3] OF STRING;

BEGIN
	arrayText[1] := 'DontShowDialogAgainCategory';
	arrayText[2] := 'DontShowDialogAgainItem'; {Should be unique for every AlertInformDontShowAgain}
	arrayText[3] := '';

	AlertInformDontShowAgain('This is an invalid item.', '', false, arrayText);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	arrayText = ('DontShowDialogAgainCategory',
				'DontShowDialogAgainItem', #{Should be unique for every AlertInformDontShowAgain}
				'')

        # python uses a tuple
	vs.AlertInformDontShowAgain('This is an invalid item.', '', False, arrayText);
Example()
```

## See Also
VS Functions:
[AlertInform](AlertInform.md) 
| [AlertQuestion](AlertQuestion.md) 
| [AlertCritical](AlertCritical.md) 
| [AlertQuestionDontShowAgain](AlertQuestionDontShowAgain.md)

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
