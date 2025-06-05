# Open

## Description
Procedure Open opens a ASCII text file for reading.

Remember to use Close when you are finished reading or writing to a file.


If the filename includes a fully qualified path, the path has to use the appropriate notation for the local operating system:
: <code>Macintosh HD:Applications:VectorWorks:Plug-Ins:Data:Notes.txt</code>
: <code>C:\Program Files\VectorWorks\Plug-Ins\Data\Notes.txt</code>


If the filename includes a path relative to the location of the VectorWorks executable, the subfolder delimiters have to be backslashes:
: <code>Plug-Ins\Data\Notes.txt</code>


If the filename does not include a path, the file is assumed to exist in the same folder as the VectorWorks executable.

```pascal
PROCEDURE Open(fileName : STRING);
```

```python
def vs.Open(fileName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|STRING|Name of file to open.|

## Remarks
Absolute paths versus relative paths:

Accepts platform specific absolute paths, or windows delimited relative paths:
*[Append](Append.md)
*[Close](Close.md)
*[EOF](EOF.md)
*[Open](Open.md)
*[Rewrite](Rewrite.md)

Accepts platform specific absolute paths only:
*[CreateFolder](CreateFolder.md)
*[GetFilesInFolder](GetFilesInFolder.md)
*[GetFolder](GetFolder.md)

Returns platform specific absolute paths (user interactive):
*[GetFile](GetFile.md)
*[GetFileN](GetFileN.md)
*[PutFile](PutFile.md)

Returns platform specific absolute paths (not user interactive):
*[GetFolderPath](GetFolderPath.md)
*[GetFPathName](GetFPathName.md)

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
fileName :STRING;
BEGIN
UseDefaultFileErrorHandling(FALSE);
fileName := 'Plug-InsCommonDataCallout Prefs.txt';
Open(fileName);
AlrtDialog(Concat(GetLastFileErr));
Close(fileName);
END;
RUN(Example);
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [File I@O](../Categories/File%20IO.md)
