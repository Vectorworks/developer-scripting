# GetLayerProjectInfo

## Description
Retrieves values similar to the Layers tab of the Project Sharing dialog.<BR>
<BR>
Timestamps are measured in seconds since January 1, 1904.  The value 0 has special meaning depending on the timestamp.

```pascal
FUNCTION GetLayerProjectInfo(
				layer                : HANDLE;
				VAR masterLayer      : BOOLEAN;
				VAR modificationDate : LONGINT;
				VAR checkoutDate     : LONGINT;
				VAR checkoutOwner    : STRING;
				VAR workingFileId    : STRING;
				VAR comment          : STRING;
				VAR outOfDate        : BOOLEAN): BOOLEAN;
```

```python
def vs.GetLayerProjectInfo(layer):
    return (BOOLEAN, masterLayer, modificationDate, checkoutDate, checkoutOwner, workingFileId, comment, outOfDate)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layer|HANDLE|Get status for this Layer|
|masterLayer|BOOLEAN|Is this layer a Master Layer, which requires higher permission to edit?|
|modificationDate|LONGINT|Timestamp of last commit.  0 means layer is unchanged since initial creation of the Project File.|
|checkoutDate|LONGINT|Timestamp of current checkout.  0 means layer is not currently checked out.|
|checkoutOwner|STRING|Userid that currently has the layer checked out.  Empty string if not checked out.|
|workingFileId|STRING|Working File Id that currently has the layer checked out.  Empty string if not checked out. This is not a filename.|
|comment|STRING|Comment for the checkout  Empty string if not checked out.|
|outOfDate|BOOLEAN|If True, there is a newer version of the layer in the Project File that can be brought in with a Refresh.|

## See Also
VS Functions:
[GetWorkingFileId](GetWorkingFileId.md) 
| [GetCurrentUserId](GetCurrentUserId.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Project Sharing](../Categories/Project%20Sharing.md)
