# GetFileN

## Description
Returns the fully-qualified pathname of the selected file.

```pascal
FUNCTION GetFileN(
				title         : STRING;
				defaultFolder : STRING;
				mask          : STRING;
				VAR fileName  : STRING): BOOLEAN;
```

```python
def vs.GetFileN(title, defaultFolder, mask):
    return (BOOLEAN, fileName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|title|STRING|   |
|defaultFolder|STRING|   |
|mask|STRING|   |
|fileName|STRING|   |

## Remarks
(*_c_* 2017.01.22): Prompts for selection of a file of type "mask". The parameter "defaultFolder", if not empty, must be a posix path (with slashes). A HFS path (with colons) to the default folders can be obtained with [GetFolderPath](GetFolderPath.md), you will need to use [ConvertHSF2PosixPath](ConvertHSF2PosixPath.md) for converting it into posix for older Vectorworks versions. Assigns the found path to var "fileName". Mask is case sensitive. The returned path is posix.
* mask = 'vwx' allows selection of files of type .vwx 
* mask = ′′ allows selection of any kind of files 
* mask = 'vwx;txt' allows range of selection (from Pat Stanford on the VS list)



The GetFileN uses the SDK interface IFileChooserDialog

[[VCOM:Working with File/Folder Choose Dialogs]]

the ‘mask’ parameter goes as input to
fileChooser->SetDefaultExtension(mask);

[[VCOM:VectorWorks:Filing:IFileChooserDialog::SetDefaultExtension]]

(MaKro, 2016.10.18):
:Mask format change in VW2016 on a Windows 7 machine
:Python mask example: '*.txt' if VW-Version < 2016 else 'txt'

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
    fileName, title : STRING; 
    defaultFolder : STRING; 
    mask : STRING; 
	
BEGIN
    title := 'Select the object library file...';
    defaultFolder := '';
    mask := 'vwx';
    pathName := 'Drafting Tools.vwx';

    IF GetFileN(title, defaultFolder, mask, pathName) THEN 
        AlrtDialog(pathName);
END;
RUN(Example);
```
#### Python ####
```python
title = 'Select the object library file...'
defaultFolder = ''
mask = 'vwx'

boo, pathName = vs.GetFileN(title, defaultFolder, mask)
if boo:
    vs.AlrtDialog(pathName)
```

## Version
Availability: from Vectorworks 2014

## Category
* [File I@O](../Categories/File%20IO.md)
