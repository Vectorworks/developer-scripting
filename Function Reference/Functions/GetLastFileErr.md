# GetLastFileErr

## Description
Returns an error code indicating whether an error occured during a file operation.

This function should be called after file I/O calls such as Open() or Rewrite().

```pascal
FUNCTION GetLastFileErr : INTEGER;
```

```python
def vs.GetLastFileErr():
    return INTEGER
```

## Remarks
Somewhere there used to be a table of return values.  we should add the table of error return values here.



Here's a more complete list:

```pascal
-1: tmpStr := 'Unspecified Error.';
0: tmpStr := 'No Err.';
1: tmpStr := 'Bad file or volume.';
2: tmpStr := 'Volume is full.';
3: tmpStr := 'File already exists.';
4: tmpStr := 'EOF reached during file read.';
5: tmpStr := 'File is locked.';
6: tmpStr := 'File or directory not found.';
7: tmpStr := 'File not open.';
8: tmpStr := 'Disk I/O Error.';
9: tmpStr := 'Volume does not exist';
10: tmpStr := 'Another read/write path is open.';
11: tmpStr := 'No write permission.';
13: tmpStr := 'Nonexistent access path.';
14: tmpStr := 'Too many files open.';
```


Only returns a read-only error if you try to write to the file and it's actually read-only. But you can read from a read-only file without getting an error.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
pathName : STRING;
fileName : STRING;
errorCode :INTEGER;
BEGIN
UseDefaultFileErrorHandling(FALSE);
Open(Concat(pathName, fileName));
errorCode := GetLastFileErr;
IF errorCode <> 0 THEN
CASE errorCode OF
2: AlrtDialog(Concat('The file "', fileName, '" cannot be processed because the hard drive is full.'));
4: AlrtDialog(Concat('End of file "',   fileName, '" reached prematurely.'));
5: AlrtDialog(Concat('The file "', fileName, '" is locked.'));
6: AlrtDialog(Concat('The file "', fileName, '" not found.'));
10: AlrtDialog(Concat('The file "', fileName, '" currently in use by another program.'));
13: AlrtDialog(Concat('The file path "', pathName, '" does not exist.'));
OTHERWISE AlrtDialog(Concat('The file "',fileName,'" has encountered an undetermined error.'));
END;
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	pathName = 'D:\'
	fileName = '_test.txt'
	vs.UseDefaultFileErrorHandling(False)
	vs.Open(vs.Concat(pathName, fileName))
	errorCode = vs.GetLastFileErr()
	if errorCode != 0:
		if errorCode == 2:
			vs.AlrtDialog(vs.Concat('The file "', fileName, '" cannot be processed because the hard drive is full.'))
		elif errorCode == 4:
			vs.AlrtDialog(vs.Concat('End of file "', fileName, '" reached prematurely.'))
		elif errorCode == 5: 
			vs.AlrtDialog(vs.Concat('The file "', fileName, '" is locked.'))
		elif errorCode == 6: 
			vs.AlrtDialog(vs.Concat('The file "', fileName, '" not found.'))
		elif errorCode == 10: 
			vs.AlrtDialog(vs.Concat('The file "', fileName, '" currently in use by another program.'))
		elif errorCode == 13: 
			vs.AlrtDialog(vs.Concat('The file path "', pathName, '" does not exist.'))
		else:
			vs.AlrtDialog(vs.Concat('The file "',fileName,'" has encountered an undetermined error.'))

Example()
```

## Version
Availability: from VectorWorks8.5

## Category
* [File I@O](../Categories/File%20IO.md)
