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

```pascal
		END;
7:	BEGIN {Shape 1 pulldown}
	tab_i := 1;
	GetSelectedChoiceInfo(dialog_ID, 7,0,temp_i,temp_s);
	IF temp_i = 4 THEN gNSides := IntDialog(GetPluginString(5008),num2str(0,gNSides));
	IF gNSides > 20 THEN BEGIN
		gNSides := 20;
		alrtdialog(getPluginString(5009));
		END;
```
```python
import vs

# Function IntDialog displays a dialog box which requests the user to enter
# an integer value.
request = 'Example'
default = 'Example'

resultN = vs.IntDialog(request, default)
vs.Message('IntDialog returned: ' + str(resultN))
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
