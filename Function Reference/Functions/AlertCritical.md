# AlertCritical

## Description
Informs the user of a serious problem that requires intervention or correction before work can continue.

```pascal
PROCEDURE AlertCritical(
				text   : STRING;
				advice : STRING);
```

```python
def vs.AlertCritical(text, advice):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|text|STRING|The information to be displayed.|
|advice|STRING|The text to be added in a smaller font under the main information message|

## Remarks
Created by TTF 1/18/2005

## Examples
[AlertDialogsAndMessages](examples/AlertDialogsAndMessages.md)

## See Also
VS Functions:
[AlertInform](AlertInform.md) 
| [AlertQuestion](AlertQuestion.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
