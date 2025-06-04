# AlertInformHLinkN

## Description
Displays an alert dialog which provides the user with information about the result of a command with an option to not show the dialog again. It offers no user choices. It provides a hyperlink (HLink) to further help the user.<BR>
<BR>
The parameter 'arrOptions' is of type ARRAY [1..3] OF STRING;<BR>
arrOpt[1] - Saved setting category to save checkbox value<BR>
arrOpt[2] - Saved setting item to save checkbox value <BR>
arrOpt[3] - Specify the string to use in overriding the default 'Dont show this dialog again' checkbox string

```pascal
PROCEDURE AlertInformHLinkN(
				text             : DYNARRAY[] of CHAR;
				adviceBeforeLink : DYNARRAY[] of CHAR;
				linkTitle        : DYNARRAY[] of CHAR;
				linkURL          : DYNARRAY[] of CHAR;
				adviceAfterLink  : DYNARRAY[] of CHAR;
				minorAlert       : BOOLEAN;
				arrOptions       : ARRAY);
```

```python
def vs.AlertInformHLinkN(text, adviceBeforeLink, linkTitle, linkURL, adviceAfterLink, minorAlert, arrOptions):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|text|DYNARRAY[] of CHAR|The information to be displayed.|
|adviceBeforeLink|DYNARRAY[] of CHAR|The text to be added in a smaller font under the main information message and above the hyperlink.|
|linkTitle|DYNARRAY[] of CHAR|The clickable text of the hyperlink to be added under the adviceBeforeLink text and above the adviceAfterLink text. The text to be added will be in the same smaller font as the adviceBeforeLink text.|
|linkURL|DYNARRAY[] of CHAR|The URL that a user will be directed to when the user clicks on the linkTitle text.|
|adviceAfterLink|DYNARRAY[] of CHAR|The text to be added under the hyperlink. The text to be added will be in the same smaller font as the adviceBeforeLink text.|
|minorAlert|BOOLEAN|The severity of the alert: minor(true) or major(false).|
|arrOptions|ARRAY|ARRAY [1..3] OF STRING; arrOpt[1] - Saved setting category to save checkbox value arrOpt[2] - Saved setting item to save checkbox value  arrOpt[3] - Specify a string to use in overriding the default 'Dont show this dialog again' checkbox string|

## Remarks
Created by KAS 8/14/2019

## Examples
```python
PROCEDURE Example;

VAR
	arrayText : ARRAY[1..3] OF STRING;

BEGIN
	arrayText[1] := 'DontShowDialogAgainCategory';
	arrayText[2] := 'DontShowDialogAgainItem'; {Should be unique for every AlertInformDontShowAgain}
	arrayText[3] := '';

	AlertInformHLinkN('This is an invalid item.', 'Please visit', 'our website', 'https://www.vectorworks.net', 'for more information on what is a valid item.', false, arrayText);
END;

RUN(Example);
```

## See Also
VS Functions:
[AlertInform](AlertInform.md) 
| [AlertQuestion](AlertQuestion.md) 
| [AlertCritical](AlertCritical.md) 
| [AlertInformDontShowAgain](AlertInformDontShowAgain.md) 
| [AlertQuestionDontShowAgain](AlertQuestionDontShowAgain.md) 
| [AlertCriticalHLink](AlertCriticalHLink.md) 
| [AlertInformHLink](AlertInformHLink.md)

## Version
Availability: from Vectorworks 2020

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
