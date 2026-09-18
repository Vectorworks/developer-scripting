# Append

## Description
Procedure Append opens the specified file for writing and appends the data to the end of the file. Existing data in the file is NOT overwritten.

If the filename includes a fully qualified path, the path has to use the appropriate notation for the local operating system:
: <code>Macintosh HD:Applications:VectorWorks:Plug-Ins:Data:Notes.txt</code>
: <code>C:\Program Files\VectorWorks\Plug-Ins\Data\Notes.txt</code>

If the filename includes a path relative to the location of the VectorWorks executable, the subfolder delimiters have to be backslashes:
: <code>Plug-Ins\Data\Notes.txt</code>

If the filename does not include a path, the file is assumed to exist in the same folder as the VectorWorks executable.

```pascal
PROCEDURE Append(fileName : STRING);
```

```python
def vs.Append(fileName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|STRING|Name of file to open for writing.|

## Examples
[FileIO](examples/FileIO.md)

```pascal
	UseDefaultFileErrorHandling(FALSE);
	Append(filename);
	IsWritable := (GetLastFileErr = 0);
	Close(filename);
END;

BEGIN
	KeyFilePathAndName := Concat(KeyTestFileFilePath, kKeyTestFileName);
	Append(Concat(KeyFilePathAndName));
	Writeln(Concat(' '));
	Writeln(Concat(TestNumNum));
END

dateLine2 := Date(2,0);
nameLine3 := 'Fur Ball';
emailLine4 := '-';
codeLine5 := '-';
Append(TheRegFile);
	WriteLn(regLine1);
	WriteLn(dateLine2);
	WriteLn(nameLine3);
	WriteLn(emailLine4);
```
```python
import vs

# Procedure Append opens the specified file for writing and appends the data
# to the end of the file.
fileName = 'C:/Temp/example.txt'

vs.Append(fileName)
```

## Version
Availability: from All Versions

## Category
* [File I@O](../Categories/File%20IO.md)
