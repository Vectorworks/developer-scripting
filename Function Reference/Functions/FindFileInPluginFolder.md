# FindFileInPluginFolder

## Description
Searches for filename in all plug-in folders.  Returns TRUE if the file is found, FALSE otherwise.  If found, the result is returned in the path parameter.

```pascal
FUNCTION FindFileInPluginFolder(
				filename : STRING;
				VAR path : STRING): BOOLEAN;
```

```python
def vs.FindFileInPluginFolder(filename):
    return (BOOLEAN, path)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filename|STRING|   |
|path|STRING|   |

## Remarks
[[User:CBM-c-|_c_]] (2016.05.16): This routine behaves differently according to where the searched file is placed:
* if a file is placed in the upper level of the User/Plug-ins folder this will always be found
* if a file is placed anywhere else (for example in a subfolder within the User/Plug-ins folder or in the Workgroup/Plug-ins folder) the routine will
** find a file only at VW launch (you need to restart VW to make the file be found)
** nevertheless it will detect immediately if the searched file is missing


On the Mac, path will use colons instead of foreslashes as the folder delimiter.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
filename, path :STRING;
BEGIN
filename := 'Callout.vso';
IF FindFileInPluginFolder(filename, path) 
THEN AlrtDialog(path)
ELSE AlrtDialog('Could not find file.');
END;
RUN(Example);
```
==== Python ====
```python
def Example():
	filename = 'Callout.vso';
	ifFileExist, path = vs.FindFileInPluginFolder(filename) 
	if ifFileExist:
		vs.AlrtDialog(path)
	else: 
		vs.AlrtDialog('Could not find file.')
		
Example()
```

## Version
Availability: from VectorWorks 12.0

## Category
* [File I@O](../Categories/File%20IO.md)
