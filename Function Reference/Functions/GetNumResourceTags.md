# GetNumResourceTags

## Description
Returns the number of tags attached to the specified resource.

```pascal
FUNCTION GetNumResourceTags(handle : HANDLE): INTEGER;
```

```python
def vs.GetNumResourceTags(handle):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|The handle to the resource|

## Examples
```pascal
resultN := GetNumResourceTags(handle);
```
```python
import vs

# Returns the number of tags attached to the specified resource.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer

count = vs.GetNumResourceTags(handle)
vs.Message('GetNumResourceTags returned: ' + str(count))
```

## See Also
VS Functions:
[SetResourceTags](SetResourceTags.md) 
| [GetResourceTags](GetResourceTags.md)

## Version
Availability: from Vectorworks 2017

## Category
* [General Edit](../Categories/General%20Edit.md)
