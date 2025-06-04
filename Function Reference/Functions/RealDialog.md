# RealDialog

## Description
Function RealDialog displays a dialog box which requests the user to enter a REAL value. RealDialog automatically screens for valid numeric input.

```pascal
FUNCTION RealDialog(
				request : STRING;
				default : STRING): REAL;
```

```python
def vs.RealDialog(request, default):
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
RealValue:=RealDialog('Enter a real value:','0.00');
```
==== Python ====
```python
realValue = vs.RealDialog('Enter a real value', '0.00')
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
