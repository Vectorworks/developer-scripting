# ResList_AddCont1

## Description
Adds a content lcoation. The 'uniqueID' is a string identifier uniquely identifying this control.

```pascal
PROCEDURE ResList_AddCont1(
				uniqueID       : STRING;
				baseFolderSpec : INTEGER;
				folderName     : DYNARRAY[] of CHAR);
```

```python
def vs.ResList_AddCont1(uniqueID, baseFolderSpec, folderName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |
|baseFolderSpec|INTEGER|   |
|folderName|DYNARRAY[] of CHAR|   |

## Examples
```pascal
ResList_Init( LocID , 16 );
ResList_AddCont1( LocID, LocBaseFolderID,LocFolderName );
ResList_Filter(LocID,Filter);
ResList_DlgInit( LocID, dialog, LocControl );
```
```python
import vs

# Adds a content lcoation.
uniqueID = 'Example'
baseFolderSpec = 1
folderName = 'C:/Temp'

vs.ResList_AddCont1(uniqueID, baseFolderSpec, folderName)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
