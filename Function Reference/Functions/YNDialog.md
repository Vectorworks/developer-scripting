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
#### VectorScript ####
```pascal
PROCEDURE Example;

VAR
	result :BOOLEAN;

BEGIN

	result := YNDialog( 'Continue?' );

END;

RUN(Example);
```
#### Python ####
```python
result = vs.YNDialog('User prompt string')
```

```pascal
	tmpStr := Concat(Chr(13), Chr(13), tmpStr, Chr(13), Chr(13));
	IF list_cnt > 1
		THEN tmpStr := Concat(GetPlugInString(7004), tmpStr, GetPlugInString(7005))
		ELSE tmpStr := Concat(GetPlugInString(7006), tmpStr, GetPlugInString(7007));
	if YNDialog(tmpStr) then for i := 1 to list_cnt DO ShowClass(list[i]);
END;

BEGIN
	target := PickObject(pt.x, pt.y);
	WHILE (target = NIL) & (YNDialog(Concat(GetPlugInString(3000), msg, GetPlugInString(3003)))) DO BEGIN
		IF msg = GetPlugInString(3001)
			THEN GetPt(pt.x, pt.y)
			ELSE GetPtL(pt1.x, pt1.y, pt.x, pt.y);
		target := PickObject(pt.x, pt.y);
	END;

BEGIN
	IF gPrefChange THEN
		IF YNDialog(kChgQuery) THEN
			UpdateSettings(2);
END;
```
```python
import vs

# Function YNDialog displays a dialog box which requests the user to select a
# Yes or No value.
s = 'Example'

ok = vs.YNDialog(s)
if ok:
    vs.Message('YNDialog succeeded')
else:
    vs.Message('YNDialog failed')
```

## Version
Availability: from All Versions

## Category
* [Dialogs - Predefined](../Categories/Dialogs%20-%20Predefined.md)
