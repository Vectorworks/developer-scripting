# GetResourceFromList

## Description
Returns the indicated resource from the indicated resource list, if the resource is in the current document.  Otherwise it returns nil.

```pascal
FUNCTION GetResourceFromList(
				listID : LONGINT;
				index  : LONGINT): HANDLE;
```

```python
def vs.GetResourceFromList(listID, index):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|listID|LONGINT|an ID for a resource list created by the BuildResourceList command.|
|index|LONGINT|an index into the list.|

## Remarks
You can check the referenced status of a resource with the object preference 700:
<code lang="pas">
IsReferenced := GetObjectVariableBoolean(handleToResourceDefinition, 700);
{locked/referenced status }
</code>

## Examples
[WorkingWithResrouceList](examples/WorkingWithResrouceList.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
