# GetWorkingFileId

## Description
Get the unique id for this Working File.  This is not a filename.<BR>
<BR>
Every Working File has a unique identifier. When layers are checked-out, they are reserved for not just a particular user, but also for a particular Working File Id.<BR>
<BR>
The reserved layer can then only be edited in that specific Working File.  If the user creates a second Working File and looks at the layer status, it will show in the second Working File as unavailable for checkout or edit, until it has been committed or released in the first file. <BR>
<BR>
The specific value of the Working File Id is not meaningful, so it is not directly visible in any of the dialogs.  It is used for the color highlighting of layer names in dialogs that show layer ownership.

```pascal
FUNCTION GetWorkingFileId(VAR uuid : STRING): BOOLEAN;
```

```python
def vs.GetWorkingFileId():
    return (BOOLEAN, uuid)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uuid|STRING|Unique id for this working file|

## See Also
VS Functions:
[GetLayerProjectInfo](GetLayerProjectInfo.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Project Sharing](../Categories/Project%20Sharing.md)
