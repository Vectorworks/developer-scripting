# AlrtDialog

## Description
Procedure AlrtDialog displays an alert dialog to the user.

```pascal
PROCEDURE AlrtDialog(message : STRING);
```

```python
def vs.AlrtDialog(message):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|message|STRING|The alert message to be displayed.|

## Remarks
If message is null, the dialog will not be displayed.

## Examples
==== VectorScript ====
```pascal
AlrtDialog('No objects are selected for this operation.');
```
==== Python ====
```python
vs.AlrtDialog('No objects are selected for this operation.')
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
