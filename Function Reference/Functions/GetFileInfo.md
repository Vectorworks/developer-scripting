# GetFileInfo

## Description
This function gets the attributes of a file.

```pascal
PROCEDURE GetFileInfo(
				filename                : STRING;
				VAR fullReadPath        : STRING;
				VAR fullWritePath       : STRING;
				VAR readFileExists      : BOOLEAN;
				VAR writeFileExists     : BOOLEAN;
				VAR locked              : BOOLEAN;
				VAR hasReadPermission   : BOOLEAN;
				VAR hasWritePermission  : BOOLEAN;
				VAR hasFolderPermission : BOOLEAN);
```

```python
def vs.GetFileInfo(filename):
    return (fullReadPath, fullWritePath, readFileExists, writeFileExists, locked, hasReadPermission, hasWritePermission, hasFolderPermission)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filename|STRING|   |
|fullReadPath|STRING|   |
|fullWritePath|STRING|   |
|readFileExists|BOOLEAN|   |
|writeFileExists|BOOLEAN|   |
|locked|BOOLEAN|   |
|hasReadPermission|BOOLEAN|   |
|hasWritePermission|BOOLEAN|   |
|hasFolderPermission|BOOLEAN|   |

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
fileName :STRING;
fullReadPath, fullWritePath :STRING;
readFileExists, writeFileExists, locked, hasReadPermission, hasWritePermission, hasFolderPermission :BOOLEAN;
BEGIN
fileName := Concat(GetFolderPath(1), 'ADINIT.DAT');
GetFileInfo(fileName, fullReadPath, fullWritePath, readFileExists, writeFileExists, locked, hasReadPermission, hasWritePermission, hasFolderPermission);
ReWrite('Output.txt');
WriteLn('fileName:            ', fileName);
WriteLn('fullReadPath:        ', fullReadPath);
WriteLn('fullWritePath:       ', fullWritePath);
WriteLn('readFileExists:      ', readFileExists);
WriteLn('writeFileExists:     ', writeFileExists);
WriteLn('locked:              ', locked);
WriteLn('hasReadPermission:   ', hasReadPermission);
WriteLn('hasWritePermission:  ', hasWritePermission);
WriteLn('hasFolderPermission: ', hasFolderPermission);
Close('Output.txt');
END;
RUN(Example);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks12.0

## Category
* [File I@O](../Categories/File%20IO.md)
