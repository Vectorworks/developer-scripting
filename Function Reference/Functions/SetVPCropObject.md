# SetVPCropObject

## Description
Sets the specified crop object in the specified viewport. If a crop object already exists, it will be replaced by the new object, so long as the new object is a valid crop.

```pascal
FUNCTION SetVPCropObject(
				viewportHandle : HANDLE;
				cropHandle     : HANDLE): BOOLEAN;
```

```python
def vs.SetVPCropObject(viewportHandle, cropHandle):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|   |
|cropHandle|HANDLE|   |

## Version
Availability: from VectorWorks11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
