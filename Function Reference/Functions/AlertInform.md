# AlertInform

## Description
Displays an alert dialog which provides the user an information about the result of a command.  It offers no user choices.

```pascal
PROCEDURE AlertInform(
				text       : STRING;
				advice     : STRING;
				minorAlert : BOOLEAN);
```

```python
def vs.AlertInform(text, advice, minorAlert):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|text|STRING|The information to be displayed.|
|advice|STRING|The text to be added in a smaller font under the main information message.|
|minorAlert|BOOLEAN|The severity of the alert: minor(true) or major(false).|

## Remarks
Created by 1/18/2005

## Examples
[AlertDialogsAndMessages](examples/AlertDialogsAndMessages.md)

## See Also
VS Functions:
[AlertQuestion](AlertQuestion.md) 
| [AlertCritical](AlertCritical.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
