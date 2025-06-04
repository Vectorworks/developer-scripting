# AddResourceToList

## Description
Adds the indicated resource to the specified resource list, if it is of the same type as the items already in the list.  Returns the index of the resource in the list or 0.

```pascal
FUNCTION AddResourceToList(
				listID   : LONGINT;
				resource : HANDLE): LONGINT;
```

```python
def vs.AddResourceToList(listID, resource):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|listID|LONGINT|an ID for a resource list created by the BuildResourceList command.|
|resource|HANDLE|a resource to add to the resource list.|

## Examples
dHatchToResource}}

## Version
Availability: from VectorWorks12.0

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
