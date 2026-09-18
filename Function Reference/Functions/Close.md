# Close

## Description
Procedure Close closes the specified text file.

If the filename includes a fully qualified path, the path has to use the appropriate notation for the local operating system:
: <code>Macintosh HD:Applications:VectorWorks:Plug-Ins:Data:Notes.txt</code>
: <code>C:\Program Files\VectorWorks\Plug-Ins\Data\Notes.txt</code>

If the filename includes a path relative to the location of the VectorWorks executable, the subfolder delimiters have to be backslashes:
: <code>Plug-Ins\Data\Notes.txt</code>

If the filename does not include a path, the file is assumed to exist in the same folder as the VectorWorks executable.

```pascal
PROCEDURE Close(fileName : STRING);
```

```python
def vs.Close(fileName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|STRING|Name of file to close.|

## Examples
[FileIO](examples/FileIO.md)

```pascal
		sizeNotFound := FALSE;
	END ELSE
		ReadLn (size1);
END;
Close (datafile);

	ValidBearingStrTest('10 30 0');
	ValidBearingStrTest('10.30.0');
	ValidBearingStrTest('10.30.30');
	WriteLn(90 - 10 - (30 / 60) - (30 / 3600));
	Close('Property Line Test.txt');
END;

BEGIN
	ReadLn( screwSize, gBoltDia, tpi, gHeadDia, gHeadHeight, gSquareWidth, gSquareHeight, gCornerRadius, gFilletR );
	sizeFound := (  screwSize = nominalSize );
END;
Close( fileName );
```
```python
import vs

# Procedure Close closes the specified text file.
fileName = 'C:/Temp/example.txt'

vs.Close(fileName)
```

## Version
Availability: from All Versions

## Category
* [File I@O](../Categories/File%20IO.md)
