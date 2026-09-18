# GetFilesInFolder

## Description
Returns the Nth filename in a folder.

```pascal
FUNCTION GetFilesInFolder(
				folderName : STRING;
				index      : INTEGER): STRING;
```

```python
def vs.GetFilesInFolder(folderName, index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|folderName|STRING|   |
|index|INTEGER|   |

## Examples
[[Python Sample Import Images as Symbols]] for example.

```pascal
While GetFilesInFolder (Concat(FldrPthAPP),Index) <> '' Do
	Begin
		FileString := GetFilesInFolder (Concat(FldrPthAPP),Index);
		ExtStr := Copy(FileString, Len(FileString) - 2, 3);
		UprString (ExtStr);

While GetFilesInFolder (Concat(FldrPthAPP),Index) <> '' DO
	BEGIN
		FileString := GetFilesInFolder (Concat(FldrPthAPP),Index);
		ExtStr := Copy(FileString, Len(FileString) - 2, 3);
		UprString (ExtStr);
```
```python
import vs

# Returns the Nth filename in a folder.
folderName = 'C:/Temp'
index = 1

text = vs.GetFilesInFolder(folderName, index)
vs.Message('GetFilesInFolder returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2014

## Category
* [File I@O](../Categories/File%20IO.md)
