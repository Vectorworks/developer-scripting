# GetFile

## Description
Procedure GetFile displays a standard file dialog which requests the user to select a text document.

It is advisable to call DidCancel after using this procedure and check that the user did not cancel the file selection process.

```pascal
PROCEDURE GetFile(VAR fileName : STRING);
```

```python
def vs.GetFile():
    return fileName
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|STRING|Returns name of selected file.|

## Remarks
At least on the Mac, fileName does not set the default folder to browse. Use GetFileN if you want this functionality.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
	fileName : STRING;
	a,b,c : INTEGER;
BEGIN
	GetFile(fileName);
	IF NOT DidCancel THEN BEGIN
		Read(a, b, c);
		Close(fileName);
	END;
END;
RUN(Example);
```
==== Python ====
```python
def Example():
	fileName = vs.GetFile()
	if not vs.DidCancel():
		vs.Read(a,b,c)
		vs.Close(fileName)


Example()
```

## Version
Availability: from All Versions

## Category
* [File I@O](../Categories/File%20IO.md)
