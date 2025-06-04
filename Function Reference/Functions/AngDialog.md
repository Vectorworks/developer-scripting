# AngDialog

## Description
Function AngDialog displays a dialog box which requests the user to enter an angle value. The dialog automatically screens for valid numeric input, and will accept supported angle formats.

```pascal
FUNCTION AngDialog(
				request : STRING;
				default : STRING): REAL;
```

```python
def vs.AngDialog(request, default):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|request|STRING|Dialog user prompt string.|
|default|STRING|Default value for input field.|

## Examples
==== VectorScript ====
```pascal
AngleValue := AngDialog('Enter an angle value:', '0d');
```
==== Python ====
```python
AngleValue = vs.AngDialog('Enter an angle value:', '0d')
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
