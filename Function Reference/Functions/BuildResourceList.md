# BuildResourceList

## Description
Creates an implicit list of  resources of a specified type, and returns an ID for the list. Values in the list can be retrieved using GetNameFromResourceList.

If the Display Default Content preference (#130) is on and folderIndex is not  0, it will also include all the resources of the specified type in all the files in the selected folder.

If folderIndex is positive, the list will include all the resources of that type from the current document, as well as from the specified folder. If folderIndex is 0, only the resources in the current document will be in the list. If folderIndex is negative, only the resources in the specified folder will be in the list.

A complete listing of supported object types may be found in the [Script Appendix](../Appendix/pages/Appendix%20D%20-%20Vectorworks%20Object%20Types%20and%20Subtypes.md).

A complete listing of supported folders may be found in the [Script Appendix](../Appendix/pages/Appendix%20J%20-%20Folder%20Indexes.md).

```pascal
FUNCTION BuildResourceList(
				type          : INTEGER;
				folderIndex   : INTEGER;
				subFolderName : STRING;
				VAR numItems  : LONGINT): LONGINT;
```

```python
def vs.BuildResourceList(type, folderIndex, subFolderName):
    return (LONGINT, numItems)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|type|INTEGER|the type of resource to put in the list|
|folderIndex|INTEGER|the index of a VW folder.|
|subFolderName|STRING|the name of a subfolder inside the folder specified by folderIndex. This can also be a partial path.  Use an empty string to request the resources from all files in the folderIndex folder.|
|numItems|LONGINT|the number of items in the list built|

## Remarks
It also will not work on any symbol which is ''inside'' a folder -- it only works on symbols at the top level.
[[User:User:KKeizer| Kars]], 26-08-2020: it is now getting all symbols including "inside" a folder and handling them as one resource list. (using VW 2020).

*\_c\_*, 2007.06.02]: This doesn't seem to support Symbol Folders (object type 92). 
[[User:User:KKeizer| Kars]], 26-08-2020: it is working with Symbol Folders (object type 92) (using VW 2020).

*\_c\_*, 2009.12.29: To obtain a list of sketch styles excluding records pass object type -47. This is to my knowledge the only usage of a negative object type.

*\_c\_*, 2016.02.29:  Here some usage examples:
```pascal
resID := 127; { wall styles }
pathID := 113; { Wall ~ Slabs folder }

list := BuildResourceList(resID, 0, '', cnt); { current document }
list := BuildResourceList(resID, pathID, '', cnt); { current document + app folder }
list := BuildResourceList(resID, -pathID, '', cnt); { current document + user folder }
```

[[User:Ptr| ptr]], 2019.09.16:

**Undocumented list id's**

| Resource type | List ID |
|---------------|---------|
| Line Types    | 96      |
| Roof Styles   | 102     |
| Slab Styles   | 107     |
| Tiles         | 108     |
| Wall Styles   | 127     |

## Examples
#### VectorScript ####
```pascal
CONST
    kHatch = 66;
    kDefHatchFolder = 105;
VAR
    listID, numItems: LONGINT;
BEGIN
    { Create a resource list of hatches from the current document and } 
    { the default hatch folder. }
    listID := BuildResourceList(kHatch, kDefHatchFolder, '', numItems);
    { ... }
```

```pascal
{ try this on a file with some symbol folders }
PROCEDURE testResCountSymFolders;
VAR
    folderList : LONGINT;
    numFolders : INTEGER;
BEGIN
    { list symbol folders in curr doc }
    folderList := BuildResourceList(92, 0, '', numFolders);
    alrtDialog(concat(numFolders));
END;
Run(testResCountSymFolders);
```
VectorScript ====
```pascal
CONST
    kHatch = 66;
    kDefHatchFolder = 105;
VAR
    listID, numItems: LONGINT;
BEGIN
    { Create a resource list of hatches from the current document and } 
    { the default hatch folder. }
    listID := BuildResourceList(kHatch, kDefHatchFolder, '', numItems);
    { ... }
```

```pascal
{ try this on a file with some symbol folders }
PROCEDURE testResCountSymFolders;
VAR
    folderList : LONGINT;
    numFolders : INTEGER;
BEGIN
    { list symbol folders in curr doc }
    folderList := BuildResourceList(92, 0, '', numFolders);
    alrtDialog(concat(numFolders));
END;
Run(testResCountSymFolders);
```

Another example from Pat Stanford <pat@coviana.com>
November 2006
[WorkingWithResrouceList](examples/WorkingWithResrouceList.md)

## See Also
VS Functions:
[AddResourceToList](AddResourceToList.md) 
| [DeleteResourceFromList](DeleteResourceFromList.md) 
| [GetNameFromResourceList](GetNameFromResourceList.md) 
| [GetResourceFromList](GetResourceFromList.md) 
| [ImportResourceToCurrentFile](ImportResourceToCurrentFile.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
