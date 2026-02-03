# ImportResToCurFileN

## Description
Imports the indicated resource from the specified list to the current file, if it is not already in the current file, and returns the handle to the resource. It will use a callback procedure to determine how to handle the duplicate resource.
The function does a comparison between the resource being imported and the resources currently in the file. If there is an exact match, then is not considered a conflict, the resource is not imported and the Callback procedure is not called.

```pascal
FUNCTION ImportResToCurFileN(
				listID   : LONGINT;
				index    : LONGINT;
				callback : PROCEDURE): HANDLE;
```

```python
def vs.ImportResToCurFileN(listID, index, callback):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|listID|LONGINT|   |
|index|LONGINT|   |
|callback|PROCEDURE|   |

## Remarks
Return values from callback determine how any conflict is handled:

eImportResourceConflictResult_DoNotImport = 0

eImportResourceConflictResult_Replace = 1

eImportResourceConflictResult_Rename = 2

The callback will be executed only when there are conflicts, and the return value will define how the conflict should be resolved (much like the radio buttons in the dialog) If you want to rename, then change the var parameter with a new unique name, otherwise it will execute the callback again.


'''January 23, 2023 Pat Stanford'''
Per forum discussion with Lada Arsenyuk of Vectorworks, we have determined that ImportRestoCurFileN does a comparison check of the resource you are attempting to import and the resources in the current file. If the resource you are trying to import is an exact duplicate of a resource in the current file, then the resource is not imported and the Callback function is not called. 

If you always want to see the conflict dialog box then use ImportResourceToCurrentFile instead.

See this thread for more discussion.

https://forum.vectorworks.net/index.php?/topic/104434-importrestocurfilen-and-callback-function/&do=findComment&comment=457282

## Examples
```pascal
PROCEDURE testResCountSymFolders;
VAR
    resList : LONGINT;
    numRes : INTEGER;
    h : HANDLE;

    FUNCTION ImportResCallback(VAR resourceName:DYNARRAY OF CHAR) : INTEGER;
        BEGIN
        AlrtDialog( resourceName );
        resourceName := Concat( resourceName , '-1' );
        ImportResCallback := 2;
        END;

BEGIN
    { list symbol folders in curr doc }
    resList := BuildResourceList(16, 23, '', numRes );
    h := ImportResToCurFileN( resList , 1, ImportResCallback );
    alrtDialog(concat('numRes=', numRes , ' h=', h));
END;
RUN(testResCountSymFolders);
```

## Version
Availability: from Vectorworks 2014

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
