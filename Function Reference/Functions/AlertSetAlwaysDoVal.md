# AlertSetAlwaysDoVal

## Description
Set the 'always do' value for the AlertQuestionDontShowAgain and AlertInformDontShowAgain standard dialogs.

```pascal
PROCEDURE AlertSetAlwaysDoVal(
				category : STRING;
				item     : STRING;
				value    : INTEGER);
```

```python
def vs.AlertSetAlwaysDoVal(category, item, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|category|STRING|category name of the value.|
|item|STRING|item name in the category.|
|value|INTEGER|new value for the default. Pass in -1 for the entry to be cleared out and the dialog to show up again.|

## See Also
VS Functions:
[AlertQuestionDontShowAgain](AlertQuestionDontShowAgain.md) 
| [AlertInformDontShowAgain](AlertInformDontShowAgain.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
