# SetResourceTags

## Description
Adds the specified tags to the specified resource.

```pascal
PROCEDURE SetResourceTags(
				handle : HANDLE;
				tags   : ARRAY);
```

```python
def vs.SetResourceTags(handle, tags):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|The handle to the resource.|
|tags|ARRAY|The list of tags.|

## Examples
```pascal
SetResourceTags(handle, tags);
```
```python
import vs

# Adds the specified tags to the specified resource.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
tags = []

vs.SetResourceTags(handle, tags)
```

## See Also
See SetObjectTags for information about returning PY tuples for the returned array.

VS Functions:
[GetResourceTags](GetResourceTags.md) 
| [GetNumResourceTags](GetNumResourceTags.md)

## Version
Availability: from Vectorworks 2017

## Category
* [General Edit](../Categories/General%20Edit.md)
