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

## Examples
```pascal
GetResourceTags(handle, tags);
```
```python
import vs

# Gets the tags attached to the specified resource.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer

result = vs.GetResourceTags(handle)
```

## See Also
See GetObjectTags for information on using PY tuples as the required array.

VS Functions:
[SetResourceTags](SetResourceTags.md) 
| [GetNumResourceTags](GetNumResourceTags.md)

## Version
Availability: from Vectorworks 2017

## Category
* [General Edit](../Categories/General%20Edit.md)
