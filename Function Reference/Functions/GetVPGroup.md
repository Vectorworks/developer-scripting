# GetVPGroup

## Description
Gets the specified viewport group.

groupType values:
Crop = 1
Annotation = 2
Cache = 3

```pascal
FUNCTION GetVPGroup(
				viewportHandle : HANDLE;
				groupType      : INTEGER): HANDLE;
```

```python
def vs.GetVPGroup(viewportHandle, groupType):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|   |
|groupType|INTEGER|   |

## Version
Availability: from VectorWorks11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
