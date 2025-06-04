# DistDialog

## Description
Function DistDialog displays a dialog box which requests the user to enter a distance value.

DistDialog automatically screens for valid numeric input.

```pascal
FUNCTION DistDialog(
				request : STRING;
				default : STRING): REAL;
```

```python
def vs.DistDialog(request, default):
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
Message(DistDialog('Enter a distance value:','0'));
```
==== Python ====
```python
vs.Message(vs.DistDialog('Enter a distance value:','0'))
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
