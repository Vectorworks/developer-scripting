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
#### VectorScript ####
```pascal
RealValue:=RealDialog('Enter a real value:','0.00');
```
#### Python ####
```python
realValue = vs.RealDialog('Enter a real value', '0.00')
```

```pascal
temp_i := 1;
if dialogType = 'AngDialog'   then temp_s := Num2Str (8, AngDialog (prompt, default)) ELSE
if dialogType = 'DistDialog'  then temp_s := Num2StrF(   DistDialog(prompt, default)) ELSE
if dialogType = 'IntDialog'   then temp_s := Num2Str (0, IntDialog (prompt, default)) ELSE
if dialogType = 'RealDialog'  then temp_s := Num2Str (8, RealDialog(prompt, default)) ELSE
IF dialogType = 'StrDialog'   THEN temp_s :=             StrDialog (prompt, default)  ELSE
IF dialogType = 'GetFolder'   THEN temp_i :=             GetFolder (prompt, default);
IF temp_i < 1 THEN BEGIN
	temp_s := default;
	RunPreDefinedDialog := (temp_i = 0);
end ELSE RunPreDefinedDialog := (NOT DidCancel);

	Num3fers := 0;
	SkipCircuit := FALSE;
	IsTwofered := FALSE;
	TwoferOverflow := FALSE;
	CirNum := RealDialog(MStr1C,Num2Str(0,CirNum));
END
```
```python
import vs

# Function RealDialog displays a dialog box which requests the user to enter
# a REAL value.
request = 'Example'
default = 'Example'

value = vs.RealDialog(request, default)
vs.Message('RealDialog returned: ' + str(value))
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
