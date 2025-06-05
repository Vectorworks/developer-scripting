# IntDialog

## Description
Function IntDialog displays a dialog box which requests the user to enter an integer value. 

IntDialog automatically screens for valid numeric input.

```pascal
FUNCTION IntDialog(
				request : STRING;
				default : STRING): INTEGER;
```

```python
def vs.IntDialog(request, default):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|request|STRING|Dialog user prompt string.|
|default|STRING|Default value for input field.|

## Examples
[SimpleDialog](examples/SimpleDialog.md)

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
