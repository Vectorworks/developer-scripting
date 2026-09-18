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
#### VectorScript ####
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
#### Python ####
```python
def example():
	request = 'User prompt string'
	default = 'Default value'
	result = vs.StrDialog(request, default)
example()
```

```pascal
BEGIN
I := 1;
While Not (DoesNotExist((Concat(kStrL,'-',I)),FALSE)) DO
	I := I+1;
TempDiaStr := StrDialog(kStrNewL,Concat(kStrL,'-',I));
	While  (Len(TempDiaStr) >64) DO
IF NOT DidCancel THEN
	BEGIN
	Sysbeep;

BEGIN
IF NOT(gWorld_Units) THEN gMult := gScaleFactor ELSE gMult := 1;
symname_s := strdialog(getpluginstring(6005),NextAvailableName(getpluginstring(6006)));
temp_h := getobject(symname_s);
{Errorcheck for duplicate name}
WHILE (temp_h <> NIL) & NOT(didcancel) DO
	BEGIN

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
```
```python
import vs

# Function StrDialog, displays a dialog box which requests the user to enter
# a string value.
request = 'Example'
default = 'Example'

text = vs.StrDialog(request, default)
vs.Message('StrDialog returned: ' + str(text))
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
