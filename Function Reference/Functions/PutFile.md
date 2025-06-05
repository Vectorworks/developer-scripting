# PutFile

## Description
Procedure PutFile displays a standard file dialog which requests the user to select or create a text file for output.

```pascal
PROCEDURE PutFile(
				commentStr   : STRING;
				defaultStr   : STRING;
				VAR fileName : STRING);
```

```python
def vs.PutFile(commentStr, defaultStr):
    return fileName
```

## Parameters
|Name|Type|Description|
|---|---|---|
|commentStr|STRING|User prompt string for dialog.|
|defaultStr|STRING|Default file name string.|
|fileName|STRING|Returns name of the user selected file.|

## Remarks
This procedure also opens the file for write, so you don't have to call Open to write to the file if PutFile was successful.

P.S. On windows, Putfile appends .txt to the file name if the entered name does not contain a file extension.  If the user enters "MyFile.mov" it will create a file called "MyFile.mov" while just entering "MyFile" will create "MyFile.txt".
Remember that you can't use any of the following chars for filenaming:  / : * ? " < > | 

On Windows, if you specify a fully qualified path in defaultStr, PutFile will default to the folder in that path, and to the file at the end of the path. On the Mac, PutFile always defaults to the folder containing the active drawing file, and defaultStr should be used just for the filename.

*_c_* (2007.08.05): PutFile fails if the file name "defaultStr" passed is longer than 31 chars (including eventual extension). The file creates but doesn't open for writing and has 0 kb. (tested only on Mac, valid for VW 12.5.+). This limit related to Mac Classic's Finder could be removed now.

## Examples
#### VectorScript ####
```pascal
PROCEDURE PutFileExample;
VAR
fileName :STRING;
BEGIN
PutFile('Select the file to create:', 'New File.txt', fileName);
Message(fileName);
IF NOT DidCancel THEN BEGIN
WriteLn('some text');
Close(fileName);
END;
END;
RUN(PutFileExample);
```
#### Python ####
```python

```

## See Also
VS Functions:
[GetLastFileErr](GetLastFileErr.md) 
| [Rewrite](Rewrite.md) 
| [GetFile](GetFile.md) 
| [Open](Open.md) 
| [Close](Close.md)

## Version
Availability: from All Versions

## Category
* [File I@O](../Categories/File%20IO.md)
