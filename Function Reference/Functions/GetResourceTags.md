# GetResourceTags

## Description
Gets the tags attached to the specified resource.

```pascal
PROCEDURE GetResourceTags(
				handle   : HANDLE;
				VAR tags : ARRAY);
```

```python
def vs.GetResourceTags(handle):
    return tags
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|The handle to the resource.|
|tags|ARRAY|The list of tags.|

## See Also
See GetObjectTags for information on using PY tuples as the required array.

VS Functions:
[SetResourceTags](SetResourceTags.md) 
| [GetNumResourceTags](GetNumResourceTags.md)

## Version
Availability: from Vectorworks 2017

## Category
* [General Edit](../Categories/General%20Edit.md)
