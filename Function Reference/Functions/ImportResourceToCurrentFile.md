# ImportResourceToCurrentFile

## Description
Imports the indicated resource from the specified list to the current file, if it is not already in the current file, and returns the handle to the resource.

```pascal
FUNCTION ImportResourceToCurrentFile(
				listID : LONGINT;
				index  : LONGINT): HANDLE;
```

```python
def vs.ImportResourceToCurrentFile(listID, index):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|listID|LONGINT|an ID for a resource list created by the [[VS:BuildResourceList]] and [[VS:BuildResourceListN]] command.|
|index|LONGINT|an index into the list.|

## Examples
[WorkingWithResrouceList](examples/WorkingWithResrouceList.md)

## See Also
VS Functions:
[ImportResToCurFileN](ImportResToCurFileN.md) | [BuildResourceList](BuildResourceList.md) |[BuildResourceListN](BuildResourceListN.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
