# YNDialog

## Description
Function YNDialog displays a dialog box which requests the user to select a Yes or No value. If the user selects the Yes button in the dialog box, the value returned by YNDialog is TRUE; if the user selects No, the function returns FALSE.

```pascal
FUNCTION YNDialog(s : STRING): BOOLEAN;
```

```python
def vs.YNDialog(s):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|s|STRING|Dialog user prompt string.|

## Remarks
YNDialog uses the exclamation icon, when really it should use the question icon.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;

VAR
	result :BOOLEAN;

BEGIN

	result := YNDialog( 'Continue?' );

END;

RUN(Example);
```
==== Python ====
```python
result = vs.YNDialog('User prompt string')
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
