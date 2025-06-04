# AlertInformHLink

## Description
Displays an alert dialog which provides the user with information about the result of a command. It offers no user choices. It provides a hyperlink (HLink) to further help the user.

```pascal
PROCEDURE AlertInformHLink(
				text             : DYNARRAY[] of CHAR;
				adviceBeforeLink : DYNARRAY[] of CHAR;
				linkTitle        : DYNARRAY[] of CHAR;
				linkURL          : DYNARRAY[] of CHAR;
				adviceAfterLink  : DYNARRAY[] of CHAR;
				minorAlert       : BOOLEAN);
```

```python
def vs.AlertInformHLink(text, adviceBeforeLink, linkTitle, linkURL, adviceAfterLink, minorAlert):
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

## Remarks
Created by KAS 8/14/2019

## Examples
```python
AlertInformHLink('That item is not a valid item', 'Please visit', 'our website', 'https://www.vectorworks.net', 'for more information on what is a valid item.', false);
```

## See Also
VS Functions:
[AlertInform](AlertInform.md) 
| [AlertQuestion](AlertQuestion.md) 
| [AlertCritical](AlertCritical.md) 
| [AlertInformDontShowAgain](AlertInformDontShowAgain.md) 
| [AlertQuestionDontShowAgain](AlertQuestionDontShowAgain.md) 
| [AlertCriticalHLink](AlertCriticalHLink.md) 
| [AlertInformHLinkN](AlertInformHLinkN.md)

## Version
Availability: from Vectorworks 2020

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
