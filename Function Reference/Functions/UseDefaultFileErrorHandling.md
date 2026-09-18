# UseDefaultFileErrorHandling

## Description
Enables or disables file I/O alert dialogs.

Use this function with GetLastFileErr() to implement custom error handling for file operations.

```pascal
PROCEDURE UseDefaultFileErrorHandling(enable : BOOLEAN);
```

```python
def vs.UseDefaultFileErrorHandling(enable):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|enable|BOOLEAN|Status of file error dialog usage.|

## Examples
```pascal
BEGIN
	tmpStatus:=TRUE;
	tmpText:=' ';
	UseDefaultFileErrorHandling(FALSE);
	Open(Concat(pathName,fileName));
	tmpCode:=GetLastFileErr;
	IF tmpCode<>0 THEN BEGIN
		tmpStatus:=FALSE;

	UseDefaultFileErrorHandling(FALSE);
	Append(filename);
	IsWritable := (GetLastFileErr = 0);
	Close(filename);
END;

BEGIN
	xmlID := InitXML;
	UseDefaultFileErrorHandling(FALSE);
	Open(xmlFile);
	IF GetLastFileErr = 0 THEN BEGIN
		Close(xmlFile);
		int := ReadXMLFile(xmlID, -1, xmlFile);
```
```python
import vs

# Enables or disables file I/O alert dialogs.
enable = True

vs.UseDefaultFileErrorHandling(enable)
```

## See Also
VS Functions:
[GetLastFileErr](GetLastFileErr.md)

## Version
Availability: from VectorWorks8.5

## Category
* [File I@O](../Categories/File%20IO.md)
