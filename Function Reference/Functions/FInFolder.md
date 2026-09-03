# FInFolder

## Description
Function FInFolder returns a handle to the first object in the referenced symbol folder. The object can be either a symbol definition or a nested symbol folder.
If the folder is empty, the function returns NIL.

```pascal
FUNCTION FInFolder(sfHd : HANDLE): HANDLE;
```

```python
def vs.FInFolder(sfHd):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sfHd|HANDLE|Handle to symbol definition or symbol folder.|

## Remarks
*\_c\_* (2017.12.25): This since VW 2017 supports all resource folders, not only symbol folders.

## Examples
```pascal
92:BEGIN
	gNumSymFolders := gNumSymFolders + 1;
	ALLOCATE gFolderN [1..gNumSymFolders];
	gFolderN [gNumSymFolders] := GetName (itemHdl);
 	 	getSymbolFolderNames (FInFolder (itemHdl));
  END;

92:BEGIN
	numSymFolders := numSymFolders + 1;
	ALLOCATE folderN [1..numSymFolders];
	folderN [numSymFolders] := GetName (itemHdl);
 	 	getSymbolFolderNames (FInFolder (itemHdl));
  END;

	END;
92: BEGIN
		saveFolderName := folderName;
		folderLevel := folderLevel + 1;
		FindAllSyms(FInFolder(symHandle), GetName(symHandle));
		folderLevel := folderLevel - 1;
		folderName := saveFolderName;
	END;
```
```python
import vs

# Function FInFolder returns a handle to the first object in the referenced
# symbol folder.
sfHd = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.FInFolder(sfHd)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
