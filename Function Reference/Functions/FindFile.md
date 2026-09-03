# FindFile

## Description
Find a file by searching the folder selector (whichPath) plus the relative file path. Searches the user folder, workgroup folders, and the app folder.

```pascal
FUNCTION FindFile(
				whichPath   : INTEGER;
				relFilePath : DYNARRAY[] of CHAR;
				VAR outPath : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.FindFile(whichPath, relFilePath):
    return (BOOLEAN, outPath)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|whichPath|INTEGER|   |
|relFilePath|DYNARRAY[] of CHAR|   |
|outPath|DYNARRAY[] of CHAR|   |

## Remarks
--~~~~June 4, 2022. Pat Stanford. OutPath MUST be a DynArray of Char. A String crashes VW to the desktop. This was also documented by Paolo in VW2020 in February 2020 on the VW Forum.

## Examples
```pascal
resultOK := FindFile(1, relFilePath, outPath);
```
```python
import vs

# Find a file by searching the folder selector (whichPath) plus the relative
# file path.
whichPath = 'C:/Temp'
relFilePath = 'C:/Temp'

ok, outPath = vs.FindFile(whichPath, relFilePath)
vs.Message('FindFile returned: ' + str((ok, outPath)))
```

## Version
Availability: from Vectorworks 2015

## Category
* [File I@O](../Categories/File%20IO.md)
