# AlertCriticalHLink

## Description
Informs the user of a serious problem that requires intervention or correction before work can continue. Provides a hyperlink (HLink) to further help the user resolve the problem.

```pascal
PROCEDURE AlertCriticalHLink(
				text             : DYNARRAY[] of CHAR;
				adviceBeforeLink : DYNARRAY[] of CHAR;
				linkTitle        : DYNARRAY[] of CHAR;
				linkURL          : DYNARRAY[] of CHAR;
				adviceAfterLink  : DYNARRAY[] of CHAR);
```

```python
def vs.AlertCriticalHLink(text, adviceBeforeLink, linkTitle, linkURL, adviceAfterLink):
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

## Remarks
Created by KAS 8/14/2019

## Examples
```python
AlertCriticalHLink('Serious Problem with X', 'Please visit', 'our website', 'https://www.vectorworks.net', 'for more information on how to resolve the problem with X.');
```

## See Also
VS Functions:
[AlertCritical](AlertCritical.md) 
| [AlertInform](AlertInform.md) 
| [AlertQuestion](AlertQuestion.md) 
| [AlertInformDontShowAgain](AlertInformDontShowAgain.md) 
| [AlertQuestionDontShowAgain](AlertQuestionDontShowAgain.md) 
| [AlertInformHLink](AlertInformHLink.md) 
| [AlertInformHLinkN](AlertInformHLinkN.md)

## Version
Availability: from Vectorworks 2020

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
