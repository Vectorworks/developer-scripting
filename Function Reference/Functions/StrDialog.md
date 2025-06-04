# StrDialog

## Description
Function StrDialog, displays a dialog box which requests the user to enter a string value.

```pascal
FUNCTION StrDialog(
				request : STRING;
				default : STRING): STRING;
```

```python
def vs.StrDialog(request, default):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|request|STRING|Dialog user prompt string.|
|default|STRING|Default value for input field.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
request, default, result :STRING;
BEGIN
request := 'User prompt string';
default := 'Default value';
result := StrDialog(request, default);
END;
RUN(Example);
```
==== Python ====
```python
def example():
	request = 'User prompt string'
	default = 'Default value'
	result = vs.StrDialog(request, default)
example()
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
